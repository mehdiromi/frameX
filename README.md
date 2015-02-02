
#FrameX

FrameX is a simple less code allows your web UI adjusted in an easy and less code. Usage: &lt;x1>this is a cell&lt;/x1> &lt;x2>this is a cell with width= 2 * x1&lt;/x2> ... &lt;x10>this is a cell with 10 * x1 width &lt;x10>


    //Define the minimum size of the desired field
    @x: 100px;
    @mar: 1px;
    @pad: 1px;
    @iterations: 16;
    .frameX(@seq)
    {
    
    width: @seq * @x  -  ( 2 * @pad)   +  (@seq - 1) * (2 * @mar) ;
    
    //background-color: @bg;
    float:left;
    margin: @mar;
    padding: @pad;   
    //font-size: 13px;
    //border: 1px solid;
    }

    .repeat(@index) when (@index > 0) {
    (~"x@{index}, .x@{index}") {
        .frameX(@index);
    }
    .repeat (@index - 1);
   }
   .repeat (0) {}
   .repeat(@iterations);
   
   
    html body * span.clear,
   .clear, 
   html body * div.clear,html body * li.clear,html body * dd.clear {
   background:none; border:0;clear:both;display:block;float:
   none;font-size:0;list-style:none;margin:0;padding:0;overflow:hidden;visibility:hidden;width:0;height:0;
   }
   
