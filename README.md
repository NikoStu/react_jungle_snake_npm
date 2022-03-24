This is a simple version of a snake game coded in ReactJS. Have fun :)

notes:
To change the style of the playboard and handheld container you can pass these in via props, use this pattern:


<Snake styles={
    {handheldBackgroundImg: "myUrl/myBackground.png",
    playboardBackgroundImg: "myUrl/myOtherBackground.png"
  }}/>,


You also have the option to receive game data (score, highscore ect.) via a function/method in the parent component, like used in this pattern:


export default function Parent(){

    function getGameData(data){
        console.log(data);
    };

    return(
        <Snake sendGameData={getGameData}/>
    );
};

