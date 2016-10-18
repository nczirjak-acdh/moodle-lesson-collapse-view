Lesson collapse view (like the lesson edit full view) for moodle 3.1 Created By Norbert Czirjak

Install steps:

1.You need to copy and overwrite the  mod/lesson/view.php and mod/lesson/renderer.php files
2. You need to add your theme header Jquery ready party the following (for the collapse function):


 /* the lesson content boxes */
            $(".box.view_pages_box tbody").hide();
            
            $(".box.view_pages_box thead").click(function(){        
                $(".box.view_pages_box tbody").hide();
                $('.generaltable.boxaligncenter thead th').css('color', '#016771');
                $('.generaltable.boxaligncenter thead th').css('background-color', 'white');
                var id = $(this).closest('table').attr('id')                
                $("#"+id+" tbody").show();
                $("#"+id+".generaltable.boxaligncenter thead th").css('color', 'white');
                $("#"+id+".generaltable.boxaligncenter thead th").css('background-color', '#016771');
            }); 
            
WARNING!!!!! These files are modifying the core lesson files!!! If there is a new moodle update then these files will be overwritten by the moodle update!!!