:root{
    --primary-color: #425b84;
    --secondary-color: #5b7bb4;
    --max-width: 1100px;
}

*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font: normal 1rem/1.5 'Arial', sans-serif;
    background: var(--primary-color);
    color: #fff;
    overflow-x: hidden;
    padding-bottom: 50px;
}

#main-header{
    background: var(--secondary-color);
    padding: 4rem 0;
}
.container{
    max-width: var(--max-width);
    margin: 0 auto;
    text-align: center; 

}
h1{
    font-size: 2.3rem;

}
#timeline ul{
background: var(--primary-color);
padding: 50px 0;
}
#timeline ul li{
    list-style: none;
    position: relative;
    width: 6px;
    margin: 0 auto;
    padding-top: 50px;
    background: #fff    ;
    /* border-radius: 50%; */
}
#timeline ul li div{
    position: relative;
    bottom: 0;
    width: 400px;
    padding: 1rem;
    background: var(--secondary-color);
    transition: all 0.5s ease-in-out;
    visibility: visible;
    opacity: 0;
}
#timeline ul li.show div{
    transform: none;
    visibility: visible;
    opacity: 1;
}

#timeline ul li:nth-child(odd) div{
    left: 40px;
    transform: translate(200px, 0);
}   
#timeline ul li:nth-child(even) div{
    left: -434px;
    transform: translate(-200px, 0);
}

#timeline ul li::after{
    content: '';
    position: absolute;
    left: 50%;
    bottom: 0;
    width: 25px;
    height: 25px;
    border-radius: 50%;
    background: var(--secondary-color);
    transform: translateX(-50%);
    transition: background 0.5s ease-in-out;
}
#timeline div::before{
    content: '';
    position: absolute;
    bottom: 5px;
    width: 0;
    height: 0;
    border-style: solid;

}
#timeline ul li:nth-child(odd) div::before{ 
    border-radius: 5px;
    left: -15px;
    border-width: 8px 16px 8px 0;
    border-color: transparent var(--secondary-color)transparent transparent;
}
#timeline ul li:nth-child(even) div::before{ 
    left: 400px;
    border-width: 8px 0 8px 16px;
    border-color: transparent transparent transparent var(--secondary-color);
}
@media (max-width: 900px) {
    #timeline ul div{
        width: 250px;

    }

    #timeline ul li:nth-child(even) div {
        left: -284px;
    }
}

