
// User vote
function rateuser(voter,candate,rate){
	
	try{
		cp.call('ajax/myphpajax.php','process_uservote',return_uservote,voter,candate,rate);
	}
	catch(Err){
		alert('Connection failed');
	}

}

function return_uservote(result){

	try{

				myMsg=result.getElementsByTagName('myMsg').item(0).firstChild.data;
				cnt=result.getElementsByTagName('cnt').item(0).firstChild.data;
				
				 showMe('himr');
				if(cnt>6){cnt=6;}	
				else if (cnt<0)	{cnt=0;}
					
				
					blank_star=6-cnt;

					var x=document.getElementById('tblViewUserVote').rows[0].cells;
					
					
					for (i=0;i<cnt;i++ )
					{
						
							x[i].innerHTML='<img src='+imgurl+'/star.gif>';
					}
					
					for (j=cnt;j<5;j++ )
					{
							x[j].innerHTML='<img src=' + imgurl+'/blank_star.gif>';
					}
				
				

				
				if(myMsg=='f'){
					var x=document.getElementById('tblViewUserTate').rows[0].cells;
					x[0].innerHTML='<B>Sorry! You already rated him.</B>';

				}else{
						var x=document.getElementById('tblViewUserTate').rows[0].cells;
 						x[0].innerHTML='<B>Thanks!</B>';
				}
				


	}
		catch(Err){
			   alert('Server prolem');
	}



					

}
// End user vote 

