bootstrap-auto-active
=====================

Simple javascript to automatically set active class on links in Bootstrap

    $('ul.nav').find('a').each(function(k,v){
        
        if( $(v).attr('href') == window.location.pathname){
            
            if($(v).parent().parent().hasClass('dropdown-menu')){
                $(v).parent().parent().parent().addClass('active');
                return;
            }

            $(v).parent().addClass('active');
        }

    });
