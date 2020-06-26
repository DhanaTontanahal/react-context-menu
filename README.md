# reactContextMenu
A Simple React Context Menu wrapped in a React component

npm i tds-reactcontextmenu

#Demo Screenshots:

![alt text](https://github.com/DhanaTontanahal/react-grid-/blob/master/context-menu-demo.PNG)


![alt text](https://github.com/DhanaTontanahal/react-grid-/blob/master/context-menu-function-call.PNG)


#Usage:
```

import React, { Component } from 'react'
import ContextMenuC from './ContextMenuC';
import styled from 'styled-components';
import {Glyphicon} from 'react-bootstrap';

const StyledContainer = styled.div`

background-color:white;
border:1px solid grey;
color:black;
font-style:italic;
z-index:9999;
width:80px;
top:10px;
left:30px;
height:auto;
position:absolute;
`;


const MyWidget = props => {

    function sortAsc(){
        alert("sortAsc ")
    }

    function sortDesc(){
        alert("sortDesc ")
    }
   
    const ContextMenu = ({ onClose }) => <StyledContainer>
        <span onClick={sortAsc}><Glyphicon glyph="glyphicon glyphicon-sort-by-attributes"/>&nbsp;<small>ascending</small></span>
        <br/><br/>
        <span onClick={sortDesc}><Glyphicon glyph="glyphicon glyphicon-sort-by-attributes-alt"/>&nbsp;<small>descending</small></span>
        <hr/>
        <button className="btn btn-danger" onClick={onClose}><Glyphicon glyph="glyphicon glyphicon-remove-circle"/></button>
    </StyledContainer>

    return <div ref={ContextMenuC.createContextMenu(ContextMenu)}>
        <b>Click here for the context menu.<Glyphicon glyph="glyphicon glyphicon-align-justify"/></b>
    </div>
    }


export default MyWidget;


```

#Column context menu usage in react table.

->Refer the below link for usage:




![alt text](https://github.com/DhanaTontanahal/react-grid-/blob/master/table1.JPG)

#Column hiding using the context menu on header click
![alt text](https://github.com/DhanaTontanahal/react-grid-/blob/master/table1.JPG)

#column reordering 
![alt text](https://github.com/DhanaTontanahal/react-grid-/blob/master/table1.JPG)





