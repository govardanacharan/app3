![Screenshot 2022-02-07 114423](https://user-images.githubusercontent.com/95639773/152736215-d32a8d7d-78eb-4f0d-b4b1-643609c7bcaf.png)
![Screenshot 2022-02-07 114423](https://user-images.githubusercontent.com/95639773/152736291-051d1796-d802-4db9-94ff-076644e73963.png)
import React from 'react';
import { useState } from 'react';
import { StyleSheet, Text, View,SafeAreaView ,ImageBackground,Image,TouchableOpacity,Button} from 'react-native';


import { ScrollView } from 'react-native';



const App = ()=> 
{
  const image= {uri:'src/images/back.png'}
    const[count,myCount]=useState(0);

 return (
     
      <View style={styles.container}>
        <ScrollView>
       
       <Text style={{textAlign:'center', marginTop:30,marginBottom:40,fontSize:20,padding:30,backgroundColor:'#ce9ffc'}}>COUNTER APPLICATION</Text>

       
       <TouchableOpacity
       style={styles.triangleShape}
       onPress={()=>{myCount(count+1)}}>
           <Text>press</Text>
     </TouchableOpacity>

     <Text style={{textAlign:'center', padding:30}}>{count}</Text>
   
     <TouchableOpacity
       style={styles.lowertriangle}
       onPress={()=>{myCount(count-1)}}>
           
     </TouchableOpacity>
     
     <TouchableOpacity title="reset" onPress={()=>{myCount(0)} 
      }  style={styles.reset}>
        
        
        <Text style={{fontSize:30}}>RESET</Text>
      </TouchableOpacity>

     
    </ScrollView>

    <Text style={styles.name}>Designed By CHARANKUMAR</Text>    
   </View>
      
  );
   
 }

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#feb672',
    //alignItems: 'center',
    //justifyContent: 'center',
  },
  triangleShape: {
    marginLeft:110,
  width: 0,
  height: 0,
  borderBottomWidth: 120,
  borderLeftWidth: 60,
  borderRightWidth: 60,
  backgroundColor: 'transparent',
  borderLeftColor: 'transparent',
  borderRightColor: 'transparent',
  borderBottomColor: '#f42e78'
},
lowertriangle: {
  marginLeft:110,
  width: 0,
  height: 0,
  borderTopWidth: 120,
  borderRightWidth: 60,
  borderLeftWidth: 60,
  borderRightColor: 'transparent',
  borderBottomColor: 'transparent',
  borderLeftColor: 'transparent',
  borderTopColor: "#f42e78",
},

reset:
{
  alignItems:'center',
  marginTop:50,
  marginRight:30,
 
},
icon:
{
  alignItems:'center',
  marginTop:-30,
  marginLeft:320,
  
},

name:
{
  textAlign:'center',
  
}



  
});

export default App;
