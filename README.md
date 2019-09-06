# playingInTurn
一个网页上实现图片轮播


轮播的边界判断（重点）
 if(img_index==3){
                img_index = 0;
            }
            else if(img_index==-1){
                img_index = 2;
            }
            
//切换图片
            $(".img").hide();
            $(".img").eq(img_index).show();
            //先全部设成白色
            $(".controls ul li").eq(img_index).css("color", "red");
            $(".controls ul li").eq(img_index).siblings().css("color", "#ffffff");
            
            
//单击小圆点事件
        $(".controls ul li").click(function () {
            //怎么才能知道点指的是哪一个
            // $(this) 当前被操作的元素（这里就是单击一个li这个操作）
            //index（）返回一组元素中，某个元素的index，从0开始
            img_index =$(this).index();
            accoord();
        });
        


