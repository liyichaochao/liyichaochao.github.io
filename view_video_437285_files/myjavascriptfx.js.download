//## !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!  SITE CONFIGURATIN !!!!!!!!!!!!!!!!!!!!!!!!!!
//!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
// DB initialization 
var dbArray = new Array();
var dbreport;
var recordcount;
var coloumcount;

// Ajax initialization 
	var cp = new cpaint();
	cp.set_debug(false);			
	cp.set_response_type('XML');	

//##!!!!!!!!!!!!!!!!!!!!!!!!!!   My FUNCTION ARCHIVE  !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
//!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

//!!!!!!!!! Executer Databse

var dbLloaded=true;

function executeDB(sql){
		var processScriptUrl=baseurl+'ajax/myphpajax.php';
		cp.call(processScriptUrl,'executeDB',return_value,sql);
	
}
	
function return_value(result){
				
		dbreport=result.getElementsByTagName('dbreport').item(0).firstChild.data;
		
		if (dbreport=='1'){
			// GET How many row fetch
			recordcount=result.getElementsByTagName('recordcount').item(0).firstChild.data;
			coloumcount=result.getElementsByTagName('coloumcount').item(0).firstChild.data;

			//Population My DB Values							
				for( i=0;i<recordcount;i++){
					dbArray[i]=new Array(recordcount);
					for( ii=0;ii<coloumcount;ii++){
						dbArray[i][ii]=result.getElementsByTagName('dbvalue'+i+ii).item(0).firstChild.data;															
					}
				}
				
				
		}


dbLoaded = false;
							
															
}
//END 

//!!!!!!!Insert data in to  table HTML patge

	function insertInToTable(tblId, varRow, varCell, varData){
		try{
			var x=document.getElementById(tblId).rows[varRow].cells;
			x[varCell].innerHTML=varData;
			return false;
		}
		catch(Err){
			return false;
		}
	}

//END 



// !!!!!! Input validation empty

	function txtBoxValidation(myId,defaultColor,errColor){
		
		// # My property
		try{	
			me=document.getElementById(myId);

			if(me.value==""){	
				me.style.background=errColor;
				me.setFocus;
				return false;
			}
			else{
				me.style.background=defaultColor;
				me.setFocus;
				return true;
			}
		}
		catch(Err){
			return 'Err';
		}
	}

// END 
 
  
// !!!! !!HIEKE A OBJECT //
function hideMe(myId){
	document.getElementById(myId).style.display="none";
	
}
// END

// !!!!!! TO SHOW A OBJECT 
function showMe(myId){
	document.getElementById(myId).style.display="block";
	
}
//END 




// !!!!!!  ASSIGN VALUE IN TO A OBJECT

function directMyvalueto(myValue,thatId){
	document.getElementById(thatId).value=myValue;
}
// END 




