var points= 0
var RED = "#E87D7B"
var YELLOW = "#FFEC62"
var GREEN = "#88E86E"
var BLUE = "#86A9FF"
var All = "lay, lay, lay, lay, lay"

//
//
///////////////////////////////////////////////////////////////////////SPLASH PAGE 1 (layspl1)
///////////////////////////////////////////////////////////////////////Create splash layout/set bg col/add image/set timer
/////////////////////////////////Would like to add "Written Using DriodScript + Logo" at the bottom.
function OnStart()
{
app.SetOrientation("Portrait");
app.SetScreenMode( "game" );
layspl1 = app.CreateLayout("Linear","VCenter,FillXY");
layspl1.SetBackColor("White");
imgmad = app.CreateImage("img/mad.png", .8);
//imgmad.SetPosition(.1,0.2);
layspl1.AddChild( imgmad );
setTimeout("timea()",3000);
app.AddLayout( layspl1 );
//Create media player.
	player1 = app.CreateMediaPlayer();
	player2= app.CreateMediaPlayer();
	player3 = app.CreateMediaPlayer();
	player4 = app.CreateMediaPlayer();
	//Load a file (can be ogg or mp3).
	player1.SetFile( "snd/MyTune.ogg" );
		player1.SetLooping( true );
	//	player1.Play()
		//
		//sound Right
	//Load a file (can be ogg or mp3).
	player2.SetFile( "snd/cha-ching.mp3" );
	//	player2.Play()
		//sound Right
	//Load a file (can be ogg or mp3).
	player3.SetFile( "snd/Poing.ogg" );
		//player3.Play()
		//
	player4.SetFile( "snd/Techno.ogg" );
 player4.SetLooping( true );

notify3 = app.CreateNotification( "AutoCancel," );
notify3.SetLargeImage( "Img/Colour Rush.png" );


}
///////////////////////////////////////////////////////////////////////SPLASH PAGE 2 (layspl2)
///////////////////////////////////////////////////////////////////////Create splash layout/set bg col/add txt/
function timea()
{
layspl2 = app.CreateLayout("Linear","VCenter,FillXY");
layspl2.Animate("FadeIn" );
layspl2.SetBackColor("#f04050");
txt = app.CreateText ("Colour", 1, null);
txt.SetFontFile("font/font1.ttf");
txt.SetTextSize(55);
txt.SetPosition(0,0);
txt.SetTextColor("White");
layspl2.AddChild(txt);
txtrush = app.CreateText ("Rush", 1, null);
//txtrush = app.CreateImage( null, 1, 0.25, "FontAwesome" );
txtrush.SetFontFile( "font/blade_runner.ttf" );
txtrush.SetTextSize(55);
txtrush.SetPosition(0,0);
txtrush.SetTextColor("White");
layspl2.AddChild(txtrush);
setTimeout("timeb()",3000);

app.AddLayout( layspl2 );
}
///////////////////////////////////////////////////////////////////////Main Screen/ Home (laymain)
///////////////////////////////////////////////////////////////////////Create Main Screen/ Add Txt/ Add Button
function timeb()
{
player4.Play(   "snd/Techno.ogg" );
laymain = app.CreateLayout("Linear","VCenter,FillXY");
laymain.Animate("FadeIn" );
laymain.SetBackColor("#f04050");
lay.SetVisibility("Hide");
laygame1.SetVisibility("Hide");
laygame.SetVisibility("Hide");
//Title
txtrush = app.CreateText ("____________________", 1, null);
//txtrush = app.CreateImage( null, 1, 0.25, "FontAwesome" );
txtrush.SetFontFile( "font/blade_runner.ttf" );
txtrush.SetTextSize(10);
txtrush.SetPosition(0,0);
txtrush.SetTextColor("White");
laymain.AddChild(txtrush);

txt = app.CreateText ("Colour", 1, null);
txt.SetFontFile("font/font1.ttf");
txt.SetTextSize(55);
txt.SetPosition(0,0);
txt.SetTextColor("White");
laymain.AddChild(txt);
txtrush = app.CreateText ("Rush", 1, null);
//txtrush = app.CreateImage( null, 1, 0.25, "FontAwesome" );
txtrush.SetFontFile( "font/blade_runner.ttf" );
txtrush.SetTextSize(55);
txtrush.SetPosition(0,0);
txtrush.SetTextColor("White");
laymain.AddChild(txtrush);

txtrush = app.CreateText ("____________________", 1, null);
//txtrush = app.CreateImage( null, 1, 0.25, "FontAwesome" );
txtrush.SetFontFile( "font/blade_runner.ttf" );
txtrush.SetTextSize(10);
txtrush.SetPosition(0,0);
txtrush.SetTextColor("White");
laymain.AddChild(txtrush);

txtrush = app.CreateText (" ", 1, null);
//txtrush = app.CreateImage( null, 1, 0.25, "FontAwesome" );
txtrush.SetFontFile( "font/blade_runner.ttf" );
txtrush.SetTextSize(50);
txtrush.SetPosition(0,0);
txtrush.SetTextColor("White");
laymain.AddChild(txtrush);

laymain.AddChild(txt);
//Play Button
btnplay = app.CreateButton ("Play", 0.95, 0.1, "");
btnplay.SetOnTouch( btnplay_OnTouch );
btnplay.SetBackColor( "#00ffffff" );
btnplay.SetFontFile( "font/font1.ttf" );
btnplay.SetTextSize( 30 );
laymain.AddChild (btnplay );

app.AddLayout( laymain );
//Instructions
btnins = app.CreateButton ("Instructions", 0.95, 0.1, "");
btnins.SetOnTouch( btnins_OnTouch );
btnins.SetBackColor( "#00ffffff" );
btnins.SetFontFile( "font/font1.ttf" );
btnins.SetTextSize( 30 );
laymain.AddChild (btnins );
app.AddLayout( laymain );
//Settings
btnset = app.CreateButton ("Settings", 0.95, 0.1, "");
btnset.SetOnTouch( btnset_OnTouch );
btnset.SetBackColor( "#00ffffff" );
btnset.SetFontFile( "font/font1.ttf" );
btnset.SetTextSize( 30 );
laymain.AddChild (btnset );
app.AddLayout( laymain );
//Credits
btncre = app.CreateButton ("Credits", 0.95, 0.1, "");
btncre.SetOnTouch( btncre_OnTouch );
btncre.SetBackColor( "#00ffffff" );
btncre.SetFontFile( "font/font1.ttf" );
btncre.SetTextSize( 30 );
laymain.AddChild (btncre );
app.AddLayout( laymain );

app.DestroyLayout(layspl1);
app.DestroyLayout(layspl2);
//app.DestroyLayout(laygame);

}


///////////////////////////////////////////////////////////////////////Game Layout/ Random Function (laygame)
///////////////////////////////////////////////////////////////////////Create Random Generator for instances (Cases)
/////////////////////////////////Would Like to add counter each time the right button is pressed...
laygame = randomLayout();

function randomLayout()
{
var ran = Math.floor( Math.random() *12) //change number to amount of instances
var laygame = app.CreateLayout ("linear");
switch(ran)
{

///////////////////////////////////////////////////////////////////////Random Generated Layout 2
///////////////////////////////////////////////////////////////////////(Word) (Text Col) ( Background Col)
case 0:

lay = app.CreateLayout("linear","VCenter, FillXY");
lay.SetVisibility("Hide");
		
//points
txtcount = app.CreateText( "" );
txtcount.SetText( points )
txtcount.SetTextColor(RED);////////////////
txtcount.SetTextSize(50);
txtcount.SetPosition(0,0.2);
lay.AddChild( txtcount );

laygame.AddChild( txtcount );
laygame.ChildToFront( txtcount );


layTop = app.CreateLayout("absolute","VCenter");
layMid = app.CreateLayout("absolute","VCenter");
layBot = app.CreateLayout("absolute","Horizontal");
lay.AddChild(layTop); /////////////////////////////////////////lay#
lay.AddChild(layMid); /////////////////////////////////////////lay#
lay.AddChild(layBot); /////////////////////////////////////////lay#
lay.SetBackColor(YELLOW);    ///////////////////////////////background & lay#
                                                   
//
txt = app.CreateText("RED");    /////////////////////////////text says
txt.SetTextColor(RED);    ////////////////////////////////text colour
txt.SetTextSize(80);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font2.ttf");
layTop.AddChild( txt );
//

//
txt = app.CreateText("Text Colour is:");  ////////////////////////Comment:
//txt = app.CreateText("Text Says Colour:");
//txt = app.CreateText("Background Colour is:");
txt.SetTextColor(RED);/////////////////////////////////////////
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layMid.AddChild( txt );
//
btnright = app.CreateButton("RED", 0.5, 0.3, "");/////////////////////
btnright.SetTextColor(RED);///////////////////////////////////////
btnright.SetOnTouch(btnright_OnTouch);
btnright.SetPosition(0,0.);
btnright.SetBackColor( "#00ffffff" );
btnright.SetFontFile( "font/font3.ttf" );
btnright.SetTextSize( 30 );
layBot.AddChild(btnright);
//
btnwrong = app.CreateButton("YELLOW", 0.5, 0.3, "");////////////////
btnwrong.SetTextColor(RED);///////////////////////////////////////
btnwrong.SetOnTouch(btnwrong_OnTouch);
btnwrong.SetPosition(0.5,0.);
btnwrong.SetBackColor( "#00ffffff" );
btnwrong.SetFontFile( "font/font3.ttf" );
btnwrong.SetTextSize( 30 );
layBot.AddChild(btnwrong);

lay.SetVisibility( "Show" );
app.AddLayout( lay );   //lay#

break;
///////////////////////////////////////////////////////////////////////Random Generated Layout 2
///////////////////////////////////////////////////////////////////////(Word) (Text Col) ( Background Col)
case 1:
		
lay = app.CreateLayout("linear","VCenter, FillXY");		
lay.SetVisibility("Hide");

//points
txtcount = app.CreateText( "" );
txtcount.SetText( points )
txtcount.SetTextColor(RED);//////////////////
txtcount.SetTextSize(50);
txtcount.SetPosition(0,0.2);
lay.AddChild( txtcount );

laygame.AddChild( txtcount );
laygame.ChildToFront( txtcount );


layTop = app.CreateLayout("absolute","VCenter");
layMid = app.CreateLayout("absolute","VCenter");
layBot = app.CreateLayout("absolute","Horizontal");
lay.AddChild(layTop);
lay.AddChild(layMid);
lay.AddChild(layBot);
lay.SetBackColor(GREEN);    //background
                                                   
//
txt = app.CreateText("RED");    //text says
txt.SetTextColor(RED);    //text colour
txt.SetTextSize(80);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font2.ttf");
layTop.AddChild( txt );
//

//
//txt = app.CreateText("Text Colour is:");
txt = app.CreateText("Text Says:");
//txt = app.CreateText("Background Colour is:");
txt.SetTextColor(RED);
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layMid.AddChild( txt );

btnwrong = app.CreateButton("GREEN", 0.5, 0.3, "");

btnwrong.SetOnTouch(btnwrong_OnTouch);
btnwrong.SetTextColor(RED);///////////////////////////////////////
btnwrong.SetPosition(0,0.);
btnwrong.SetBackColor( "#00ffffff" );
btnwrong.SetFontFile( "font/font3.ttf" );
btnwrong.SetTextSize( 30 );
layBot.AddChild(btnwrong);
//
btnright = app.CreateButton("RED", 0.5, 0.3, "");
btnright.SetTextColor(RED);///////////////////////////////////////
btnright.SetOnTouch(btnright_OnTouch);
btnright.SetPosition(0.5,0.);
btnright.SetBackColor( "#00ffffff" );
btnright.SetFontFile( "font/font3.ttf" );
btnright.SetTextSize( 30 );
layBot.AddChild(btnright);
//


lay.SetVisibility( "Show" );
app.AddLayout( lay );

break;
///////////////////////////////////////////////////////////////////////Random Generated Layout 3
///////////////////////////////////////////////////////////////////////(Word) (Text Col) ( Background Col)
case 2:
		
lay = app.CreateLayout("linear","VCenter, FillXY");		
lay.SetVisibility("Hide");

//points
txtcount = app.CreateText( "" );
txtcount.SetText( points )
txtcount.SetTextColor(RED);//////////////////
txtcount.SetTextSize(50);
txtcount.SetPosition(0,0.2);
lay.AddChild( txtcount );

laygame.AddChild( txtcount );
laygame.ChildToFront( txtcount );


layTop = app.CreateLayout("absolute","VCenter");
layMid = app.CreateLayout("absolute","VCenter");
layBot = app.CreateLayout("absolute","Horizontal");
lay.AddChild(layTop);
lay.AddChild(layMid);
lay.AddChild(layBot);
lay.SetBackColor(BLUE);    //background
                                                   
//
txt = app.CreateText("RED");    //text says
txt.SetTextColor(RED);    //text colour
txt.SetTextSize(80);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font2.ttf");
layTop.AddChild( txt );
//

//
//txt = app.CreateText("Text Colour is:");
//txt = app.CreateText("Text Says:");
txt = app.CreateText("Background Colour is:");
txt.SetTextColor(RED);
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layMid.AddChild( txt );

btnwrong = app.CreateButton("RED", 0.5, 0.3, "");//////////
btnwrong.SetOnTouch(btnwrong_OnTouch);
btnwrong.SetTextColor(RED);///////////////////////////////////////
btnwrong.SetPosition(0,0.);
btnwrong.SetBackColor( "#00ffffff" );
btnwrong.SetFontFile( "font/font3.ttf" );
btnwrong.SetTextSize( 30 );
layBot.AddChild(btnwrong);
//
btnright = app.CreateButton("BLUE", 0.5, 0.3, "");
btnright.SetTextColor(RED);///////////////////////////////////////
btnright.SetOnTouch(btnright_OnTouch);
btnright.SetPosition(0.5,0.);
btnright.SetBackColor( "#00ffffff" );
btnright.SetFontFile( "font/font3.ttf" );
btnright.SetTextSize( 30 );
layBot.AddChild(btnright);
//
lay.SetVisibility( "Show" );
app.AddLayout( lay );

break;
///////////////////////////////////////////////////////////////////////Random Generated Layout 2
///////////////////////////////////////////////////////////////////////(Word) (Text Col) ( Background Col)
case 3:

lay = app.CreateLayout("linear","VCenter, FillXY");
lay.SetVisibility("Hide");
		
//points
txtcount = app.CreateText( "" );
txtcount.SetText( points )
txtcount.SetTextColor(RED);////////////////
txtcount.SetTextSize(50);
txtcount.SetPosition(0,0.2);
lay.AddChild( txtcount );

laygame.AddChild( txtcount );
laygame.ChildToFront( txtcount );


layTop = app.CreateLayout("absolute","VCenter");
layMid = app.CreateLayout("absolute","VCenter");
layBot = app.CreateLayout("absolute","Horizontal");
lay.AddChild(layTop); /////////////////////////////////////////lay#
lay.AddChild(layMid); /////////////////////////////////////////lay#
lay.AddChild(layBot); /////////////////////////////////////////lay#
lay.SetBackColor(YELLOW);    ///////////////////////////////background & lay#
                                                   
//
txt = app.CreateText("YELLOW");    /////////////////////////////text says
txt.SetTextColor(RED);    ////////////////////////////////text colour
txt.SetTextSize(80);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font2.ttf");
layTop.AddChild( txt );
//

//
txt = app.CreateText("Text Colour is:");  ////////////////////////Comment:
//txt = app.CreateText("Text Says:");
//txt = app.CreateText("Background Colour is:");
txt.SetTextColor(RED);/////////////////////////////////////////
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layMid.AddChild( txt );
//
btnright = app.CreateButton("RED", 0.5, 0.3, "");/////////////////////
btnright.SetTextColor(RED);///////////////////////////////////////
btnright.SetOnTouch(btnright_OnTouch);
btnright.SetPosition(0.5,0.);
btnright.SetBackColor( "#00ffffff" );
btnright.SetFontFile( "font/font3.ttf" );
btnright.SetTextSize( 30 );
layBot.AddChild(btnright);
//
btnwrong = app.CreateButton("YELLOW", 0.5, 0.3, "");////////////////
btnwrong.SetTextColor(RED);///////////////////////////////////////
btnwrong.SetOnTouch(btnwrong_OnTouch);
btnwrong.SetPosition(0,0.);
btnwrong.SetBackColor( "#00ffffff" );
btnwrong.SetFontFile( "font/font3.ttf" );
btnwrong.SetTextSize( 30 );
layBot.AddChild(btnwrong);

lay.SetVisibility( "Show" );
app.AddLayout( lay );   //lay#

break;
///////////////////////////////////////////////////////////////////////Random Generated Layout 2
///////////////////////////////////////////////////////////////////////(Word) (Text Col) ( Background Col)
case 4:
		
lay = app.CreateLayout("linear","VCenter, FillXY");		
lay.SetVisibility("Hide");

//points
txtcount = app.CreateText( "" );
txtcount.SetText( points )
txtcount.SetTextColor(RED);//////////////////
txtcount.SetTextSize(50);
txtcount.SetPosition(0,0.2);
lay.AddChild( txtcount );

laygame.AddChild( txtcount );
laygame.ChildToFront( txtcount );


layTop = app.CreateLayout("absolute","VCenter");
layMid = app.CreateLayout("absolute","VCenter");
layBot = app.CreateLayout("absolute","Horizontal");
lay.AddChild(layTop);
lay.AddChild(layMid);
lay.AddChild(layBot);
lay.SetBackColor(GREEN);    //background
                                                   
//
txt = app.CreateText("YELLOW");    //text says
txt.SetTextColor(RED);    //text colour
txt.SetTextSize(80);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font2.ttf");
layTop.AddChild( txt );
//

//
//txt = app.CreateText("Text Colour is:");
txt = app.CreateText("Text Says:");
//txt = app.CreateText("Background Colour is:");
txt.SetTextColor(RED);
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layMid.AddChild( txt );

btnwrong = app.CreateButton("GREEN", 0.5, 0.3, "");
btnwrong.SetOnTouch(btnwrong_OnTouch);
btnwrong.SetTextColor(RED);///////////////////////////////////////
btnwrong.SetPosition(0.5,0.);
btnwrong.SetBackColor( "#00ffffff" );
btnwrong.SetFontFile( "font/font3.ttf" );
btnwrong.SetTextSize( 30 );
layBot.AddChild(btnwrong);
//
btnright = app.CreateButton("YELLOW", 0.5, 0.3, "");
btnright.SetTextColor(RED);///////////////////////////////////////
btnright.SetOnTouch(btnright_OnTouch);
btnright.SetPosition(0,0.);
btnright.SetBackColor( "#00ffffff" );
btnright.SetFontFile( "font/font3.ttf" );
btnright.SetTextSize( 30 );
layBot.AddChild(btnright);
//


lay.SetVisibility( "Show" );
app.AddLayout( lay );

break;

///////////////////////////////////////////////////////////////////////End of Game Layout/ Random Function (laygame)
///////////////////////////////////////////////////////////////////////Random Generated Layout 2
///////////////////////////////////////////////////////////////////////(Word) (Text Col) ( Background Col)
case 5:
		
lay = app.CreateLayout("linear","VCenter, FillXY");		
lay.SetVisibility("Hide");

//points
txtcount = app.CreateText( "" );
txtcount.SetText( points )
txtcount.SetTextColor(RED);//////////////////
txtcount.SetTextSize(50);
txtcount.SetPosition(0,0.2);
lay.AddChild( txtcount );

laygame.AddChild( txtcount );
laygame.ChildToFront( txtcount );


layTop = app.CreateLayout("absolute","VCenter");
layMid = app.CreateLayout("absolute","VCenter");
layBot = app.CreateLayout("absolute","Horizontal");
lay.AddChild(layTop);
lay.AddChild(layMid);
lay.AddChild(layBot);
lay.SetBackColor(BLUE);    //background
                                                   
//
txt = app.CreateText("YELLOW");    //text says
txt.SetTextColor(RED);    //text colour
txt.SetTextSize(80);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font2.ttf");
layTop.AddChild( txt );
//

//
//txt = app.CreateText("Text Colour is:");
//txt = app.CreateText("Text Says:");
txt = app.CreateText("Background Colour is:");
txt.SetTextColor(RED);
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layMid.AddChild( txt );

btnwrong = app.CreateButton("RED", 0.5, 0.3, "");
btnwrong.SetOnTouch(btnwrong_OnTouch);
btnwrong.SetTextColor(RED);///////////////////////////////////////
btnwrong.SetPosition(0.5,0.);
btnwrong.SetBackColor( "#00ffffff" );
btnwrong.SetFontFile( "font/font3.ttf" );
btnwrong.SetTextSize( 30 );
layBot.AddChild(btnwrong);
//
btnright = app.CreateButton("BLUE", 0.5, 0.3, "");
btnright.SetTextColor(RED);///////////////////////////////////////
btnright.SetOnTouch(btnright_OnTouch);
btnright.SetPosition(0,0.);
btnright.SetBackColor( "#00ffffff" );
btnright.SetFontFile( "font/font3.ttf" );
btnright.SetTextSize( 30 );
layBot.AddChild(btnright);
//

lay.SetVisibility( "Show" );
app.AddLayout( lay );

break;

////////////////////////////////////////////////////////////
///////////////////////////////////////////////////////////////////////Random Generated Layout 2
///////////////////////////////////////////////////////////////////////(Word) (Text Col) ( Background Col)
case 6:
		
lay = app.CreateLayout("linear","VCenter, FillXY");		
lay.SetVisibility("Hide");

//points
txtcount = app.CreateText( "" );
txtcount.SetText( points )
txtcount.SetTextColor(RED);//////////////////
txtcount.SetTextSize(50);
txtcount.SetPosition(0,0.2);
lay.AddChild( txtcount );

laygame.AddChild( txtcount );
laygame.ChildToFront( txtcount );


layTop = app.CreateLayout("absolute","VCenter");
layMid = app.CreateLayout("absolute","VCenter");
layBot = app.CreateLayout("absolute","Horizontal");
lay.AddChild(layTop);
lay.AddChild(layMid);
lay.AddChild(layBot);
lay.SetBackColor(YELLOW);    //background
                                                   
//
txt = app.CreateText("GREEN");    //text says
txt.SetTextColor(RED);    //text colour
txt.SetTextSize(80);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font2.ttf");
layTop.AddChild( txt );
//

//
txt = app.CreateText("Text Colour is:");
//txt = app.CreateText("Text Says:");
//txt = app.CreateText("Background Colour is:");
txt.SetTextColor(RED);
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layMid.AddChild( txt );

btnwrong = app.CreateButton("GREEN", 0.5, 0.3, "");
btnwrong.SetOnTouch(btnwrong_OnTouch);
btnwrong.SetTextColor(RED);///////////////////////////////////////
btnwrong.SetPosition(0.5,0.);
btnwrong.SetBackColor( "#00ffffff" );
btnwrong.SetFontFile( "font/font3.ttf" );
btnwrong.SetTextSize( 30 );
layBot.AddChild(btnwrong);
//
btnright = app.CreateButton("RED", 0.5, 0.3, "");
btnright.SetTextColor(RED);///////////////////////////////////////
btnright.SetOnTouch(btnright_OnTouch);
btnright.SetPosition(0,0.);
btnright.SetBackColor( "#00ffffff" );
btnright.SetFontFile( "font/font3.ttf" );
btnright.SetTextSize( 30 );
layBot.AddChild(btnright);
//


lay.SetVisibility( "Show" );
app.AddLayout( lay );

break;

////////////////////////////////////////////////////////////
///////////////////////////////////////////////////////////////////////Random Generated Layout 2
///////////////////////////////////////////////////////////////////////(Word) (Text Col) ( Background Col)
case 7:
		
lay = app.CreateLayout("linear","VCenter, FillXY");		
lay.SetVisibility("Hide");

//points
txtcount = app.CreateText( "" );
txtcount.SetText( points )
txtcount.SetTextColor(RED);//////////////////
txtcount.SetTextSize(50);
txtcount.SetPosition(0,0.2);
lay.AddChild( txtcount );

laygame.AddChild( txtcount );
laygame.ChildToFront( txtcount );


layTop = app.CreateLayout("absolute","VCenter");
layMid = app.CreateLayout("absolute","VCenter");
layBot = app.CreateLayout("absolute","Horizontal");
lay.AddChild(layTop);
lay.AddChild(layMid);
lay.AddChild(layBot);
lay.SetBackColor(GREEN);    //background
                                                   
//
txt = app.CreateText("GREEN");    //text says
txt.SetTextColor(RED);    //text colour
txt.SetTextSize(80);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font2.ttf");
layTop.AddChild( txt );
//

//
//txt = app.CreateText("Text Colour is:");
txt = app.CreateText("Text Says:");
//txt = app.CreateText("Background Colour is:");
txt.SetTextColor(RED);
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layMid.AddChild( txt );

btnwrong = app.CreateButton("RED", 0.5, 0.3, "");
btnwrong.SetOnTouch(btnwrong_OnTouch);
btnwrong.SetTextColor(RED);///////////////////////////////////////
btnwrong.SetPosition(0.5,0.);
btnwrong.SetBackColor( "#00ffffff" );
btnwrong.SetFontFile( "font/font3.ttf" );
btnwrong.SetTextSize( 30 );
layBot.AddChild(btnwrong);
//
btnright = app.CreateButton("GREEN", 0.5, 0.3, "");
btnright.SetTextColor(RED);///////////////////////////////////////
btnright.SetOnTouch(btnright_OnTouch);
btnright.SetPosition(0,0.);
btnright.SetBackColor( "#00ffffff" );
btnright.SetFontFile( "font/font3.ttf" );
btnright.SetTextSize( 30 );
layBot.AddChild(btnright);
//


lay.SetVisibility( "Show" );
app.AddLayout( lay );

break;

////////////////////////////////////////////////////////////
///////////////////////////////////////////////////////////////////////Random Generated Layout 2
///////////////////////////////////////////////////////////////////////(Word) (Text Col) ( Background Col)
case 8:
		
lay = app.CreateLayout("linear","VCenter, FillXY");		
lay.SetVisibility("Hide");

//points
txtcount = app.CreateText( "" );
txtcount.SetText( points )
txtcount.SetTextColor(RED);//////////////////
txtcount.SetTextSize(50);
txtcount.SetPosition(0,0.2);
lay.AddChild( txtcount );

laygame.AddChild( txtcount );
laygame.ChildToFront( txtcount );


layTop = app.CreateLayout("absolute","VCenter");
layMid = app.CreateLayout("absolute","VCenter");
layBot = app.CreateLayout("absolute","Horizontal");
lay.AddChild(layTop);
lay.AddChild(layMid);
lay.AddChild(layBot);
lay.SetBackColor(BLUE);    //background
                                                   
//
txt = app.CreateText("GREEN");    //text says
txt.SetTextColor(RED);    //text colour
txt.SetTextSize(80);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font2.ttf");
layTop.AddChild( txt );
//

//
//txt = app.CreateText("Text Colour is:");
//txt = app.CreateText("Text Says:");
txt = app.CreateText("Background Colour is:");
txt.SetTextColor(RED);
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layMid.AddChild( txt );

btnwrong = app.CreateButton("GREEN", 0.5, 0.3, "");
btnwrong.SetOnTouch(btnwrong_OnTouch);
btnwrong.SetTextColor(RED);///////////////////////////////////////
btnwrong.SetPosition(0.5,0.);
btnwrong.SetBackColor( "#00ffffff" );
btnwrong.SetFontFile( "font/font3.ttf" );
btnwrong.SetTextSize( 30 );
layBot.AddChild(btnwrong);
//
btnright = app.CreateButton("BLUE", 0.5, 0.3, "");
btnright.SetTextColor(RED);///////////////////////////////////////
btnright.SetOnTouch(btnright_OnTouch);
btnright.SetPosition(0,0.);
btnright.SetBackColor( "#00ffffff" );
btnright.SetFontFile( "font/font3.ttf" );
btnright.SetTextSize( 30 );
layBot.AddChild(btnright);
//


lay.SetVisibility( "Show" );
app.AddLayout( lay );

break;

////////////////////////////////////////////////////////////
///////////////////////////////////////////////////////////////////////Random Generated Layout 2
///////////////////////////////////////////////////////////////////////(Word) (Text Col) ( Background Col)
case 9:
		
lay = app.CreateLayout("linear","VCenter, FillXY");		
lay.SetVisibility("Hide");

//points
txtcount = app.CreateText( "" );
txtcount.SetText( points )
txtcount.SetTextColor(RED);//////////////////
txtcount.SetTextSize(50);
txtcount.SetPosition(0,0.2);
lay.AddChild( txtcount );

laygame.AddChild( txtcount );
laygame.ChildToFront( txtcount );


layTop = app.CreateLayout("absolute","VCenter");
layMid = app.CreateLayout("absolute","VCenter");
layBot = app.CreateLayout("absolute","Horizontal");
lay.AddChild(layTop);
lay.AddChild(layMid);
lay.AddChild(layBot);
lay.SetBackColor(YELLOW);    //background
                                                   
//
txt = app.CreateText("BLUE");    //text says
txt.SetTextColor(RED);    //text colour
txt.SetTextSize(80);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font2.ttf");
layTop.AddChild( txt );
//

//
txt = app.CreateText("Text Colour is:");
//txt = app.CreateText("Text Says:");
//txt = app.CreateText("Background Colour is:");
txt.SetTextColor(RED);
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layMid.AddChild( txt );

btnwrong = app.CreateButton("YELLOW", 0.5, 0.3, "");
btnwrong.SetOnTouch(btnwrong_OnTouch);
btnwrong.SetTextColor(RED);///////////////////////////////////////
btnwrong.SetPosition(0.5,0.);
btnwrong.SetBackColor( "#00ffffff" );
btnwrong.SetFontFile( "font/font3.ttf" );
btnwrong.SetTextSize( 30 );
layBot.AddChild(btnwrong);
//
btnright = app.CreateButton("RED", 0.5, 0.3, "");
btnright.SetTextColor(RED);///////////////////////////////////////
btnright.SetOnTouch(btnright_OnTouch);
btnright.SetPosition(0,0.);
btnright.SetBackColor( "#00ffffff" );
btnright.SetFontFile( "font/font3.ttf" );
btnright.SetTextSize( 30 );
layBot.AddChild(btnright);
//


lay.SetVisibility( "Show" );
app.AddLayout( lay );

break;

////////////////////////////////////////////////////////////
///////////////////////////////////////////////////////////////////////Random Generated Layout 2
///////////////////////////////////////////////////////////////////////(Word) (Text Col) ( Background Col)
case 10:
		
lay = app.CreateLayout("linear","VCenter, FillXY");		
lay.SetVisibility("Hide");

//points
txtcount = app.CreateText( "" );
txtcount.SetText( points )
txtcount.SetTextColor(RED);//////////////////
txtcount.SetTextSize(50);
txtcount.SetPosition(0,0.2);
lay.AddChild( txtcount );

laygame.AddChild( txtcount );
laygame.ChildToFront( txtcount );


layTop = app.CreateLayout("absolute","VCenter");
layMid = app.CreateLayout("absolute","VCenter");
layBot = app.CreateLayout("absolute","Horizontal");
lay.AddChild(layTop);
lay.AddChild(layMid);
lay.AddChild(layBot);
lay.SetBackColor(GREEN);    //background
                                                   
//
txt = app.CreateText("BLUE");    //text says
txt.SetTextColor(RED);    //text colour
txt.SetTextSize(80);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font2.ttf");
layTop.AddChild( txt );
//

//
txt = app.CreateText("Text Colour is:");
//txt = app.CreateText("Text Says:");
//txt = app.CreateText("Background Colour is:");
txt.SetTextColor(RED);
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layMid.AddChild( txt );

btnwrong = app.CreateButton("GREEN", 0.5, 0.3, "");
btnwrong.SetOnTouch(btnwrong_OnTouch);
btnwrong.SetTextColor(RED);///////////////////////////////////////
btnwrong.SetPosition(0.5,0.);
btnwrong.SetBackColor( "#00ffffff" );
btnwrong.SetFontFile( "font/font3.ttf" );
btnwrong.SetTextSize( 30 );
layBot.AddChild(btnwrong);
//
btnright = app.CreateButton("BLUE", 0.5, 0.3, "");
btnright.SetTextColor(RED);///////////////////////////////////////
btnright.SetOnTouch(btnright_OnTouch);
btnright.SetPosition(0,0.);
btnright.SetBackColor( "#00ffffff" );
btnright.SetFontFile( "font/font3.ttf" );
btnright.SetTextSize( 30 );
layBot.AddChild(btnright);
//


lay.SetVisibility( "Show" );
app.AddLayout( lay );

break;

////////////////////////////////////////////////////////////
///////////////////////////////////////////////////////////////////////Random Generated Layout 2
///////////////////////////////////////////////////////////////////////(Word) (Text Col) ( Background Col)
case 11:
		
lay = app.CreateLayout("linear","VCenter, FillXY");		
lay.SetVisibility("Hide");

//points
txtcount = app.CreateText( "" );
txtcount.SetText( points )
txtcount.SetTextColor(RED);//////////////////
txtcount.SetTextSize(50);
txtcount.SetPosition(0,0.2);
lay.AddChild( txtcount );

laygame.AddChild( txtcount );
laygame.ChildToFront( txtcount );


layTop = app.CreateLayout("absolute","VCenter");
layMid = app.CreateLayout("absolute","VCenter");
layBot = app.CreateLayout("absolute","Horizontal");
lay.AddChild(layTop);
lay.AddChild(layMid);
lay.AddChild(layBot);
lay.SetBackColor(BLUE);    //background
                                                   
//
txt = app.CreateText("BLUE");    //text says
txt.SetTextColor(RED);    //text colour
txt.SetTextSize(80);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font2.ttf");
layTop.AddChild( txt );
//

//
//txt = app.CreateText("Text Colour is:");
//txt = app.CreateText("Text Says:");
txt = app.CreateText("Background Colour is:");
txt.SetTextColor(RED);
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layMid.AddChild( txt );

btnwrong = app.CreateButton("RED", 0.5, 0.3, "");
btnwrong.SetOnTouch(btnwrong_OnTouch);
btnwrong.SetTextColor(RED);///////////////////////////////////////
btnwrong.SetPosition(0.5,0.);
btnwrong.SetBackColor( "#00ffffff" );
btnwrong.SetFontFile( "font/font3.ttf" );
btnwrong.SetTextSize( 30 );
layBot.AddChild(btnwrong);
//
btnright = app.CreateButton("BLUE", 0.5, 0.3, "");
btnright.SetTextColor(RED);///////////////////////////////////////
btnright.SetOnTouch(btnright_OnTouch);
btnright.SetPosition(0,0.);
btnright.SetBackColor( "#00ffffff" );
btnright.SetFontFile( "font/font3.ttf" );
btnright.SetTextSize( 30 );
layBot.AddChild(btnright);
//


lay.SetVisibility( "Show" );
app.AddLayout( lay );

break;
}
////////////////////////////////////////////////////////////


return laygame;
}
//////////////////////////////
//////////////////////////////
laygame1 = app.CreateLayout("linear","VCenter, FillXY");		
laygame1.SetBackColor("#f04050");
app.AddLayout( laygame1 );


///////////////////////////////////////////////////////////////////////TimeOut
///////////////////////////////////////////////////////////////////////Create splash layout/set bg col/add txt/
function timeup()
{



 laygame.DestroyChild( btnright );
 laygame.DestroyChild( btnwrong );
 
 
 
 
 
 laygame1.SetVisibility("Show");
 

laytime = app.CreateLayout("linear","VCenter,FillXY");
laytime.SetBackColor("#f04050");
txt = app.CreateText ("TIME UP!", 1, null);
laytime.SetVisibility("Hide");
//app.DestroyLayout(laygame);
laytime.Animate("slideFromTop");



txt.SetTextSize(60);
txt.SetPosition(0,0.4);
txt.SetFontFile("font/font1.tff");
txt.SetTextColor("White");
laytime.AddChild(txt);

player1.Stop();


txt = app.CreateText ("Your Score:", 1, null);
txt.SetTextSize(30);
txt.SetPosition(0,0.4);
txt.SetFontFile("font/font1.tff");
txt.SetTextColor("White");
laytime.AddChild(txt);

//score
txtcount = app.CreateText( "" );
txtcount.SetText( points )
txtcount.SetTextColor("white");
txtcount.SetTextSize(20);
txtcount.SetPosition(0,0.2);
this.highScore = scores;
laytime.AddChild( txtcount );


btnreset= app.CreateButton("TRY AGAIN", 0.5, 0.3, "");
btnreset.SetOnTouch(btnreset_OnTouch);
btnreset.SetPosition(0.5,0.);
btnreset.SetBackColor( "#00ffffff" );
btnreset.SetFontFile( "font/font1.ttf" );
btnreset.SetTextSize( 30 );
laytime.AddChild(btnreset);

btnresetmain= app.CreateButton("HOME", 0.5, 0.3, "");
btnresetmain.SetOnTouch(btnresetmain_OnTouch);
btnresetmain.SetPosition(0.5,0.);
btnresetmain.SetBackColor( "#00ffffff" );
btnresetmain.SetFontFile( "font/font1.ttf" );
btnresetmain.SetTextSize( 30 );
laytime.AddChild(btnresetmain);


var scores = app.LoadText("highscores", "{}"); 
highScores = JSON.parse(scores);

app.AddLayout( laytime );
}

///////////////////////////////////////////////////////////////////////Instructions
///////////////////////////////////////////////////////////////////////Create splash layout/set bg col/add txt/

layins = app.CreateLayout("linear","VCenter,FillXY");
layins.SetVisibility("Hide");
layins.SetBackColor("#f04050");
txt = app.CreateText("Instructions");    //text says
txt.SetTextColor("white");    //text colour
txt.SetTextSize(40);
txt.SetPosition(0.2,0);
txt.SetFontFile( "font/blade_runner.ttf" );
layins.AddChild( txt );
//space
txt = app.CreateText(" ");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(40);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layins.AddChild( txt );
//
txt = app.CreateText("You Have 60 Seconds To");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layins.AddChild( txt );
txt = app.CreateText("Collect as many points");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layins.AddChild( txt );
txt = app.CreateText("As possible, read the");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layins.AddChild( txt );
txt = app.CreateText("Instructions Carefully");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layins.AddChild( txt );
txt = app.CreateText("Before Time Runs Out!");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layins.AddChild( txt );
//space
txt = app.CreateText("");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layins.AddChild( txt );

txt = app.CreateText("+1 Point For a Correct Answer");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layins.AddChild( txt );
txt = app.CreateText("-5 Point For a Wrong Answer");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layins.AddChild( txt );

btnhomeins = app.CreateButton("Main Menu", 0.5, 0.3, "");
btnhomeins.SetOnTouch(btnhomeins_OnTouch);
btnhomeins.SetPosition(0.5,0.);
btnhomeins.SetBackColor( "#00ffffff" );
btnhomeins.SetFontFile( "font/font1.ttf" );
btnhomeins.SetTextSize( 30 );
layins.AddChild(btnhomeins);

app.AddLayout( layins );

///////////////////////////////////////////////////////////////////////Settings
///////////////////////////////////////////////////////////////////////Create splash layout/set bg col/add txt/

layset = app.CreateLayout("linear","VCenter,FillXY");
layset.SetVisibility("Hide");
layset.SetBackColor("#f04050");

txt = app.CreateText("Settings");    //text says
txt.SetTextColor("white");    //text colour
txt.SetTextSize(40);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/blade_runner.ttf" );
layset.AddChild( txt );
//
txt = app.CreateText(" ");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(40);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layset.AddChild( txt );
//
txt = app.CreateText("Settings Coming Soon...");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
layset.AddChild( txt );

btnhomeset= app.CreateButton("Main Menu", 0.5, 0.3, "");
btnhomeset.SetOnTouch(btnhomeset_OnTouch);
btnhomeset.SetPosition(0.5,0.);
btnhomeset.SetBackColor( "#00ffffff" );
btnhomeset.SetFontFile( "font/font1.ttf" );
btnhomeset.SetTextSize( 30 );
layset.AddChild(btnhomeset);

app.AddLayout( layset );

///////////////////////////////////////////////////////////////////////Credits
///////////////////////////////////////////////////////////////////////Create splash layout/set bg col/add txt/

laycre = app.CreateLayout("linear","VCenter,FillXY");
laycre.SetVisibility("Hide");
laycre.SetBackColor("#f04050");

txt = app.CreateText("Credits");    //text says
txt.SetTextColor("white");    //text colour
txt.SetTextSize(40);
txt.SetPosition(0,0);
txt.SetFontFile( "font/blade_runner.ttf" );
laycre.AddChild( txt );
//

//
txt = app.CreateText(" ");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(40);
txt.SetPosition(0,0);
txt.SetFontFile( "font/font1.ttf");
laycre.AddChild( txt );

txt = app.CreateText("This game was created using");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
laycre.AddChild( txt );

txt = app.CreateText(" ");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(30);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
laycre.AddChild( txt );

txt = app.CreateText("DroidScript");
imgdroid = app.CreateImage("img/droid.png", 0.2);
txt = app.CreateText(" ");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(30);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
laycre.AddChild( txt );
//imgmad.SetPosition(.1,0.2);
laycre.AddChild( imgdroid);
txt.SetTextColor("#99ffffff");
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
laycre.AddChild( txt );

txt = app.CreateText(" ");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(30);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
laycre.AddChild( txt );

txt = app.CreateText("Special Thanks To;");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
laycre.AddChild( txt );

txt = app.CreateText("Steve Garman");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
laycre.AddChild( txt );

txt = app.CreateText("&");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
laycre.AddChild( txt );

txt = app.CreateText("Symbroson Development");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
laycre.AddChild( txt );

txt = app.CreateText("For their help during development of Quick Pick!");
txt.SetTextColor("#99ffffff");
txt.SetTextSize(15);
txt.SetPosition(0,0.2);
txt.SetFontFile( "font/font3.ttf");
laycre.AddChild( txt );

btnhomecre = app.CreateButton("Main Menu", 0.5, 0.3, "");
btnhomecre.SetOnTouch(btnhomecre_OnTouch);
btnhomecre.SetPosition(0.5,0.);
btnhomecre.SetBackColor( "#00ffffff" );
btnhomecre.SetFontFile( "font/font1.ttf" );
btnhomecre.SetTextSize( 30 );
laycre.AddChild(btnhomecre);

app.AddLayout( laycre );























///////////////////////////////////////////////////////////////////////Button functions
function btnplay_OnTouch()
{
player1.SeekTo( 0 );
player1.Play();
player4.Stop();
laygame= randomLayout();
points = points == 0;
txtcount.SetText( 0 )
//layspl1.SetVisibility("Hide");
//layspl2.SetVisibility("Hide"); 
layins.SetVisibility("Hide");
layset.SetVisibility("Hide");
laycre.SetVisibility("Hide");
laygame1.SetVisibility("Hide");
//laygame.SetVisibility("Show");
//lay.SetVisibility("Show");
lay.Animate("FadeIn");
laymain.Animate("FadeOut");
laygame.Animate("FadeIn");
app.Vibrate( "0,100" );
setTimeout("timeup()", 60000);
}

function btnright_OnTouch()
{
app.Vibrate( "0,10" );
lay.Animate( "FadeOut" );
player2.SeekTo( 0 );
player2.Play();
btnright.SetBackColor( "white" );
points = points + 1;
laygame.DestroyChild(lay);
laygame = randomLayout();
laygame.Animate( "FadeIn" );
//laygame.Animate("SlideFromRight");
//app.AddLayout(laygame);

}

function btnwrong_OnTouch()
{
app.Vibrate( "0,10,0,10" );
lay.Animate( "FadeOut" );
//laygame.SetVisibility("Hide");
player3.SeekTo( 0 );
player3.Play();
btnwrong.SetBackColor( "red" );
points = points - 5;
laygame.DestroyChild(lay);
laygame = randomLayout();
laygame.Animate( "FadeIn" );
//app.DestroyDrawer( laygame );
//app.RemoveDrawer(  laygame );
}

function OnPause()
{
player1.Pause()
player2.Pause()
player3.Pause()
player4.Pause()
//app.Exit();
 // app.ShowPopup( "Press your Home button and wait a few seconds" );
    setTimeout( DelayedNotify, 6000 );
    app.Vibrate( "0,100" );
}

//Set (delayed) notification.
function DelayedNotify()
{
notify3.SetMessage( "Full screen notification!", "Nice Score Loser! XD", "Hey, your score wasnt that bad, loser! Come back and prove me wrong!" );
notify3.SetLargeImage( "Img/colour rush.png" );
notify3.Notify();      
//notify3.vibrate("10");
}


function btnhomeins_OnTouch()
{
//app.DestroyLayout(laygame);
lay.
laymain.Animate("FadeIn");
app.Vibrate( "0,10" );
layins.Animate("FadeOut");
//layspl1.SetVisibility("Hide");
//layspl2.SetVisibility("Hide");
//app.DestroyLayout( laytime );
//app.DestroyLayout( laygame );
//app.Exit();
}

function btnhomeset_OnTouch()
{
//app.DestroyLayout(laygame);
layset.Animate("FadeOut");
app.Vibrate( "0,10" );
laymain.Animate("FadeIn");
//layspl1.SetVisibility("Hide");
//layspl2.SetVisibility("Hide");
//app.DestroyLayout( laytime );
//app.DestroyLayout( laygame );
//app.Exit();
}

function btnhomecre_OnTouch()
{
//app.DestroyLayout(laygame);
laycre.Animate("FadeOut");
app.Vibrate( "0,10" );
laymain.Animate("FadeIn");
//layspl1.SetVisibility("Hide");
//layspl2.SetVisibility("Hide");
//app.DestroyLayout( laytime );
//app.DestroyLayout( laygame );
//app.Exit();
}

function btnreset_OnTouch()
{
app.DestroyLayout(laygame);
laygame= randomLayout();
points = points == 0;
txtcount.SetText( 0 )
//laygame.Animate("SlideToRight");
laytime.Animate("SlideToRight");
app.Vibrate( "0,10" );
//laymain.SetVisibility("Show");
player1.SeekTo( 0 );
player1.Play();
//layspl1.SetVisibility("Hide");
//layspl2.SetVisibility("Hide");
layins.SetVisibility("Hide");
layset.SetVisibility("Hide");
laycre.SetVisibility("Hide");
laymain.Animate("SlideToRight");
setTimeout("timeup()", 60000);
//laygame.Animate("SlideFromLeft");
//app.DestroyLayout( laytime );
//app.Exit();
}


function btnresetmain_OnTouch()
{
app.DestroyLayout(laygame);
//laygame.RemoveChild( "lay" );
//laygame.RemoveChild( "lay" );
//laygame.RemoveChild( "lay" );
//laygame.RemoveChild( "lay" );
lay.SetVisibility("Hide");
laygame1.SetVisibility("Hide");
laygame.SetVisibility("Hide");
//laygame.RemoveChild( "lay" );
//laygame.RemoveChild( "laytop" );
//laygame.RemoveChild( "laymid" );
//laygame.RemoveChild( "laybot" );
//laymain.RemoveChild( laymain );
//laymain.AddChild( laymain );
//app.DestroyLayout(laygame);
//laygame.Animate("SlideToRight");
laytime.Animate("FadeOut");
//laygame.Animate("FadeOut");
//laygame.Hide(laygame);
app.Vibrate( "0,10" );
//laymain.SetVisibility("Show");
//layspl1.SetVisibility("Hide");
//layspl2.SetVisibility("Hide");
//laymain.ChildToFront( laymain );
laymain.Animate("FadeIn");
//setTimeout("timeup()", 60000);
//laygame.Animate("SlideFromLeft");
//app.DestroyLayout( laytime );
//app.Exit();
}

function btnins_OnTouch()
{
//layspl1.SetVisibility("Hide");
//layspl2.SetVisibility("Hide");
laymain.Animate("FadeOut");
app.Vibrate( "0,10" );
layins.Animate("FadeIn");

//app.DestroyLayout( laytime );
//app.DestroyLayout( laygame );
//app.Exit();
}

function btncre_OnTouch()
{
//layspl1.SetVisibility("Hide");
//layspl2.SetVisibility("Hide");
laymain.Animate("FadeOut");
app.Vibrate( "0,10" );
laycre.Animate("FadeIn");
//app.DestroyLayout( laytime );
//app.DestroyLayout( laygame );
//app.Exit();
}


function btnset_OnTouch()
{
//layspl1.SetVisibility("Hide");
//layspl2.SetVisibility("Hide");
laymain.Animate("FadeOut");
app.Vibrate( "0,10" );
layset.Animate("FadeIn");

//app.DestroyLayout( laytime );
//app.DestroyLayout( laygame );
//app.Exit();
}
