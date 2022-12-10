<html>

    <head>

        <style>

            .song{

                display:list-item;

                border: none;

                background-color: black;

                color: white;

                padding: 8px;

                transform: color;

                

                transition-duration: 2s;

            }

            .song:hover{

                color: blue;

                

                

            }

            .song:hover ~ .so{

                transform: opacity(.5);

            }

            #t{

                box-shadow:  0px 10px 50px darkblue;

                display: none;              

                

            }

            

            #menu{

                display: none;

            }

        </style>

        <script>

            function my(){

               var v=document.getElementById("select");

               let w=0;

               

               

               var freader=new FileReader();

               

               freader.readAsDataURL(v.files[0]);

               freader.onloadend=function(event){

                var r=document.getElementById("audio");

                r.src=event.target.result;

                var h= event.target.result;

               }

               let c=0;

                for(l=0;l<v.files.length;l++)

                {

                    var v=document.getElementById("select");

                    var s=document.createElement("button");

                    let y=v.files[l].name;

                    y=`${y}`

                    

                    y=y.replace("[iSongs.info]"," ")

                    y=y.replace(".mp3"," ")

                    let e=document.createTextNode(y);

                    

                    s.appendChild(e);

                    

                    document.getElementById("so").appendChild(s).setAttribute("id",`${c}`);

                    document.getElementById(`${c}`).className="song";

                    document.getElementById(`${c}`).setAttribute("value",`${c}`);

                    let g=document.getElementById(`${c}`).value;

                    document.getElementById(`${c}`).onclick=function(){iu(g)};

                    

                    c=c+1;

                   

                }

                document.getElementById("import").style.display="none";

                document.getElementById("menu").style.display="inline";

            }

              

              

            

            

            function y(){

                var v=document.getElementById("select");

                var r=document.getElementById("audio");

                document.getElementById("import").style.display="none";

                document.getElementById("play").style.display="none";

                document.getElementById("pause").style.display="inline-block";

                r.play();

                r.onended=function(){

                    var v=document.getElementById("select");

                

                if(i==0)

                {

                    var freader=new FileReader();

               

               freader.readAsDataURL(v.files[0]);

               freader.onloadend=function(event){

                var r=document.getElementById("audio");

                r.src=event.target.result;

                

                i=i+1;

                

                r.play();

                }

                y();

               }

               else if(i<v.files.length-1)

               {

                var freader=new FileReader();

               

               freader.readAsDataURL(v.files[i]);

               freader.onloadend=function(event){

                var r=document.getElementById("audio");

                r.src=event.target.result;

               

                i=i+1;

                r.play();

                }

                y();

               }

               else{

                var freader=new FileReader();

               

               freader.readAsDataURL(v.files[i]);

               freader.onloadend=function(event){

                var r=document.getElementById("audio");

                r.src=event.target.result;

                

                

                i=0;

                r.play();

               }}

                };

                

              }

              let i=0;

              let w=0;

               function next(){

                var v=document.getElementById("select");

                

                if(i==0)

                {

                    var freader=new FileReader();

               

               freader.readAsDataURL(v.files[0]);

               freader.onloadend=function(event){

                var r=document.getElementById("audio");

                r.src=event.target.result;

                

                i=i+1;

                

                r.play();

                }

                y();

               }

               else if(i<v.files.length-1)

               {

                var freader=new FileReader();

               

               freader.readAsDataURL(v.files[i]);

               freader.onloadend=function(event){

                var r=document.getElementById("audio");

                r.src=event.target.result;

               

                i=i+1;

                r.play();

                }

                y();

               }

               else{

                var freader=new FileReader();

               

               freader.readAsDataURL(v.files[i]);

               freader.onloadend=function(event){

                var r=document.getElementById("audio");

                r.src=event.target.result;

                

                

                i=0;

                r.play();

               }

               y();

            }

            }

            function prev(){

                var v=document.getElementById("select");

                if(i==0)

                {

                    i=v.files.length-1;

                   

                    var freader=new FileReader();

                    freader.readAsDataURL(v.files[i]);

                    freader.onloadend=function(event){

                        var r=document.getElementById("audio");

                        r.src=event.target.result;

                        r.play();

                    }

                    console.log(i)

                    y();

                    

                    

                }

                else if(i<=v.files.length-1)

                {

                    i--;

                    var freader = new FileReader();

                    freader.readAsDataURL(v.files[i]);

                    freader.onloadend=function(event){

                        var r= document.getElementById("audio");

                        r.src=event.target.result;

                        r.play();

                        }

                        

                        y();

                       

                    }

                

                else{

                    i=0;

                    var freader = new FileReader();

                    freader.readAsDataURL(v.files[i]);

                    freader.onloadend=function(event){

                        var r = document.getElementById("audio");

                        r.src=event.target.result;

                        r.play();

                    }

                    console.log(i)



                    y();

                }

            }

            function search(){

                var f=document.getElementById("select");

                let input=document.getElementById("search").value;

                input=input.toLowerCase();

                let x=document.getElementsByClassName("song");

                for(i=0;i<x.length;i++)

                {

                    if(!x[i].innerHTML.toLowerCase().includes(input))

                    {

                        x[i].style.display="none";

                    }

                    else

                    {

                        x[i].style.display="list-item"

                    }

                }}

                function u(){

                    var v=document.getElementById("select");

                    for(r=0;r<=v.files.length;r++)

                    {

                        let w=document.getElementById("fileno").value;

                        console.log(w);

                        if(w==r)

                        {

                            var filereader=new FileReader();

                filereader.readAsDataURL(v.files[w-1]);

                filereader.onloadend=function(event){

                    var a=document.getElementById("audio");

                    a.src=event.target.result;

                    document.getElementById("audio").play();

                    i=w-1;

                         }

                        }

                    }



                    document.getElementById("import").style.display="none";

                }

                function iu(id){

                    

                    var v=document.getElementById("select");

                    var filereader=new FileReader();

                filereader.readAsDataURL(v.files[id]);

                filereader.onloadend=function(event){

                    var a=document.getElementById("audio");

                    a.src=event.target.result;

                    document.getElementById("audio").play();

                    

                 var r=a;

                    document.getElementById("play").style.display="none";

                document.getElementById("pause").style.display="inline-block";

                r.onended=function(){

                    var v=document.getElementById("select");

                

                if(id==0)

                {

                    var freader=new FileReader();

               

               freader.readAsDataURL(v.files[0]);

               freader.onloadend=function(event){

                var r=document.getElementById("audio");

                r.src=event.target.result;

                

                id=id+1;

                

                r.play();

                }

                y();

               }

               else if(id<v.files.length-1)

               {

                var freader=new FileReader();

               

               freader.readAsDataURL(v.files[id]);

               freader.onloadend=function(event){

                var r=document.getElementById("audio");

                r.src=event.target.result;

               

                id=id+1;

                r.play();

                }

                y();

               }

               else{

                var freader=new FileReader();

               

               freader.readAsDataURL(v.files[id]);

               freader.onloadend=function(event){

                var r=document.getElementById("audio");

                r.src=event.target.result;

                

                

                id=0;

                r.play();

               }}

                };

                }}

                function pause(){

                    document.getElementById("pause").style.display="none";

                    document.getElementById("play").style.display="inline-block";

                    var r=document.getElementById("audio");

                    r.pause();

                }

                function menu(){

                    document.getElementById("t").style.display="flex";

                    document.getElementById("menu").style.display="none";

                    document.getElementById("menu1").style.display="inline";

                }

                function menu1(){

                    document.getElementById("t").style.display="none";

                    document.getElementById("menu").style.display="inline";

                    document.getElementById("menu1").style.display="none";

                }

                function name(){

                   let er=prompt("Enter Your Name");

                    document.getElementById("name").innerHTML="Welcome To Off-Line Music Player "+ er.toUpperCase();

                }

            </script>

    </head>

    <body style="background-color:blanchedalmond;" onload="name()">

        <h1 style="color:coral; background-color:seashell; position:fixed; top:0;left:43%; border-radius:10px; font-family:Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;">

            <span style="font-size: 60px;">O</span><span>F</span>F-LINE   <span style="color: none; margin-left: 10px;"><span style="font-size: 50px;">  M</span>USIC <span style="font-size: 40px;">P</span>LAYER</span>

        </h1>

        <h5 id="name" style="position: fixed; top: 80px; left: 48%;color :gold; background-color:seashell; ">

            

        </h5>

        <div style="height: 30px; width: 50px; border: none; background-color: blanchedalmond;position: fixed; top: 50px;" id="menu" onclick="menu()"><span style="color:white;background-color: blanchedalmond; fill:currentColor;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><!--! Font Awesome Pro 6.2.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M0 96C0 78.3 14.3 64 32 64H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32H32c-17.7 0-32-14.3-32-32s14.3-32 32-32H416c17.7 0 32 14.3 32 32z"/></svg></span></div>

        <div style="height: 30px; width: 50px; border: none; background-color: blanchedalmond;position: fixed; top: 5px; left: 450px; display: none;" id="menu1" onclick="menu1()"><span style="color:white;background-color: blanchedalmond; fill:currentColor;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><!--! Font Awesome Pro 6.2.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M0 96C0 78.3 14.3 64 32 64H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32H32c-17.7 0-32-14.3-32-32s14.3-32 32-32H416c17.7 0 32 14.3 32 32z"/></svg></span></div>



        <div id="import" style="position: fixed; top:45%; left:43%; height:200px;width:400px;background-color:burlywood; border-radius: 0px 15px 0px 15px; ">

        

        <center ">

        <input type="file" id="select" multiple accept=".mp3" style="position: relative; margin-top: 80px;">

        <input type="submit" onclick="my()">

    </center>

        

    </div>

    <div id="t" style="margin-left:0%; margin-top: 0px; height: auto; width: 400px; background-color: black;">

        <ol class="so" id="so">

            

        </ol>

    

    </div>

    <div>

        <audio controls id="audio" style="position: fixed; bottom:60px; left:45%;">

            <source src="">

        </audio>

        

        <div style="position: fixed; bottom:0px;left:49%;">

        <button onclick="prev()" style="height: 30px; width: 50px; border: none; background-color: blanchedalmond;"><span style="color:white;background-color: blanchedalmond; fill:currentColor;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><!--! Font Awesome Pro 6.2.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M459.5 440.6c9.5 7.9 22.8 9.7 34.1 4.4s18.4-16.6 18.4-29V96c0-12.4-7.2-23.7-18.4-29s-24.5-3.6-34.1 4.4L288 214.3V256v41.7L459.5 440.6zM256 352V256 128 96c0-12.4-7.2-23.7-18.4-29s-24.5-3.6-34.1 4.4l-192 160C4.2 237.5 0 246.5 0 256s4.2 18.5 11.5 24.6l192 160c9.5 7.9 22.8 9.7 34.1 4.4s18.4-16.6 18.4-29V352z"/></svg></span></button>

        <button onclick="y()" id="play" style="height: 30px; width: 50px; border: none; background-color: blanchedalmond;"><span  style="color: white; background-color: blanchedalmond; fill:currentColor; "><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512" style="background-color:blanchedalmond;"><!--! Font Awesome Pro 6.2.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M73 39c-14.8-9.1-33.4-9.4-48.5-.9S0 62.6 0 80V432c0 17.4 9.4 33.4 24.5 41.9s33.7 8.1 48.5-.9L361 297c14.3-8.7 23-24.2 23-41s-8.7-32.2-23-41L73 39z"/></svg></span></button>

        <button onclick="pause()" id="pause" style="height: 30px; width: 50px; border: none; background-color: blanchedalmond; display: none;"><span  style="color: white; background-color: blanchedalmond; fill:currentColor; "><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"><!--! Font Awesome Pro 6.2.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M48 64C21.5 64 0 85.5 0 112V400c0 26.5 21.5 48 48 48H80c26.5 0 48-21.5 48-48V112c0-26.5-21.5-48-48-48H48zm192 0c-26.5 0-48 21.5-48 48V400c0 26.5 21.5 48 48 48h32c26.5 0 48-21.5 48-48V112c0-26.5-21.5-48-48-48H240z"/></svg></span></button>

        <button onclick="next()" style="height:30px; width:50px; border: none; background-color: blanchedalmond;"><span style="color: white; background-color: blanchedalmond; fill:currentColor; "><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><!--! Font Awesome Pro 6.2.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M52.5 440.6c-9.5 7.9-22.8 9.7-34.1 4.4S0 428.4 0 416V96C0 83.6 7.2 72.3 18.4 67s24.5-3.6 34.1 4.4L224 214.3V256v41.7L52.5 440.6zM256 352V256 128 96c0-12.4 7.2-23.7 18.4-29s24.5-3.6 34.1 4.4l192 160c7.3 6.1 11.5 15.1 11.5 24.6s-4.2 18.5-11.5 24.6l-192 160c-9.5 7.9-22.8 9.7-34.1 4.4s-18.4-16.6-18.4-29V352z"/></svg></span></button>

    </div>

    </div>

        <div style="height: 300px; width:200px; margin-left: 45%; position: fixed;top: 100px; right: 200px;">

            <input type="search" id="search" onkeypress="search()" placeholder="search song" style="color: black; border-radius: 5px; background-color: white;">

            

            

        </div>

    </body>

</html>
