<HTML>
    <HEAD>
        <TITLE>
            Basic Sudoku Game
        </TITLE>
        
        <STYLE>
            table
            {
                width=300; 
                height=300;
                padding: 10px;
                border: 1px solid black;
                border-collapse:collapse;
                margin: auto
            }
            
            input {
                width: 50px; 
                height: 50px;
                text-align:center;
            }
            
            button {
                
            }
        </STYLE>
    </HEAD>
        <BODY>
            <DIV>
                <TABLE>
                    <TR>
                        <TD >
                            <TABLE>
                                <TR>
                                    <TD>
                                        <input type="text" id="cell11" name="cell11" placeholder="5" disabled="disabled" align="middle">
                                    </TD>
                                    
                                     <TD>
                                         <input type="text" id="cell12" name="cell12" placeholder="3" disabled="disabled">
                                    </TD>
                                    
                                     <TD>
                                         <input type="text" id="cell13" name="cell13" onblur="checkInput(0, 2, 0, this.value, this.id)" onclick="resetBlock(0, 2, 0, this.value, this.id)">
                                    </TD>
                                </TR>
                                
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell21" name="cell21" placeholder="6" disabled="disabled">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell22" name="cell22" onblur="checkInput(1, 1, 0, this.value, this.id)" onclick="resetBlock(1, 1, 0, this.value, this.id)">   
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell23" name="cell23" onblur="checkInput(1, 2, 0, this.value, this.id)" onclick="resetBlock(1, 2, 0, this.value, this.id)">
                                    </TD>
                                </TR>
                                
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell31" name="cell31" onblur="checkInput(2, 0, 0, this.value, this.id)" onclick="resetBlock(2, 0, 0, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell32" name="cell32" onblur="checkInput(2, 1, 0, this.value, this.id)"  placeholder="9" disabled="disabled">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell33" name="cell33" onblur="checkInput(2, 2, 0, this.value, this.id)"  placeholder="8" disabled="disabled">
                                    </TD>
                                </TR>
                            </TABLE>
                        </TD>
                        <TD>
                            <TABLE>
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell14" name="cell14" onblur="checkInput(0, 3, 1, this.value, this.id)" onclick="resetBlock(0, 3, 1, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell15" name="cell15" onblur="checkInput(0, 4, 1, this.value, this.id)"  placeholder="7" disabled="disabled">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell16" name="cell16" onblur="checkInput(0, 5, 1, this.value, this.id)" onclick="resetBlock(0, 5, 1, this.value, this.id)">
                                    </TD>
                                </TR>
                                
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell24" name="cell24" onblur="checkInput(1, 3, 1, this.value, this.id)"  placeholder="1" disabled="disabled">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell25" name="cell25" onblur="checkInput(1, 4, 1, this.value, this.id)"  placeholder="9" disabled="disabled">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell26" name="cell26" onblur="checkInput(1, 5, 1, this.value, this.id)"  placeholder="5" disabled="disabled">
                                    </TD>
                                </TR>
                                
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell34" name="cell34" onblur="checkInput(2, 3, 1, this.value, this.id)" onclick="resetBlock(2, 3, 1, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell35" name="cell35" onblur="checkInput(2, 4, 1, this.value, this.id)" onclick="resetBlock(2, 4, 1, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell36" name="cell36" onblur="checkInput(2, 5, 1, this.value, this.id)" onclick="resetBlock(2, 5, 1, this.value, this.id)">
                                    </TD>
                                </TR>
                            </TABLE>
                        </TD>
                        <TD>
                            <TABLE>
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell17" name="cell17" onblur="checkInput(0, 6, 2, this.value, this.id)" onclick="resetBlock(0, 6, 2, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell18" name="cell18" onblur="checkInput(0, 7, 2, this.value, this.id)" onclick="resetBlock(0, 7, 2, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell19" name="cell19" onblur="checkInput(0, 8, 2, this.value, this.id)" onclick="resetBlock(0, 8, 2, this.value, this.id)">
                                    </TD>
                                </TR>
                                
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell27" name="cell27" onblur="checkInput(1, 6, 2, this.value, this.id)" onclick="resetBlock(1, 6, 2, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell28" name="cell28" onblur="checkInput(1, 7, 2, this.value, this.id)" onclick="resetBlock(1, 7, 2, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell29" name="cell29" onblur="checkInput(1, 8, 2, this.value, this.id)" onclick="resetBlock(1, 8, 2, this.value, this.id)">
                                    </TD>
                                </TR>
                                
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell37" name="cell37" onblur="checkInput(2, 6, 2, this.value, this.id)" onclick="resetBlock(2, 6, 2, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell38" name="cell38" onblur="checkInput(2, 7, 2, this.value, this.id)"  placeholder="6" disabled="disabled">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell39" name="cell39" onblur="checkInput(2, 8, 2, this.value, this.id)" onclick="resetBlock(2, 8, 2, this.value, this.id)">
                                    </TD>
                                </TR>
                            </TABLE>
                        </TD>
                    </TR>
                    
                    <TR>
                        <TD>
                            <TABLE>
                                <TR>
                                    <TD >
                                        <input  type="text" id="cell41" name="cell41" onblur="checkInput(3, 0, 3, this.value, this.id)"  placeholder="8" disabled="disabled">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell42" name="cell42" onblur="checkInput(3, 1, 3, this.value, this.id)" onclick="resetBlock(3, 1, 3, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell43" name="cell43" onblur="checkInput(3, 2, 3, this.value, this.id)" onclick="resetBlock(3, 2, 3, this.value, this.id)">
                                    </TD>
                                </TR>
                                
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell51" name="cell51" onblur="checkInput(4, 0, 3, this.value, this.id)"  placeholder="4" disabled="disabled">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell52" name="cell52" onblur="checkInput(4, 1, 3, this.value, this.id)" onclick="resetBlock(4, 1, 3, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell53" name="cell53" onblur="checkInput(4, 2, 3, this.value, this.id)" onclick="resetBlock(4, 2, 3, this.value, this.id)">
                                    </TD>
                                </TR>
                                
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell61" name="cell61" onblur="checkInput(5, 0, 3, this.value, this.id)"  placeholder="7" disabled="disabled">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell62" name="cell62" onblur="checkInput(5, 1, 3, this.value, this.id)" onclick="resetBlock(5, 1, 3, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell63" name="cell63" onblur="checkInput(5, 2, 3, this.value, this.id)" onclick="resetBlock(5, 2, 3, this.value, this.id)">
                                    </TD>
                                </TR>
                            </TABLE>
                        </TD>
                        <TD>
                            <TABLE>
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell44" name="cell44" onblur="checkInput(3, 3, 4, this.value, this.id)" onclick="resetBlock(3, 3, 4, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell45" name="cell45" onblur="checkInput(3, 4, 4, this.value, this.id)"  placeholder="6" disabled="disabled">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell46" name="cell46" onblur="checkInput(3, 5, 4, this.value, this.id)" onclick="resetBlock(3, 5, 4, this.value, this.id)">
                                    </TD>
                                </TR>
                                
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell54" name="cell54" onblur="checkInput(4, 3, 4, this.value, this.id)"  placeholder="8" disabled="disabled">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell55" name="cell55" onblur="checkInput(4, 4, 4, this.value, this.id)" onclick="resetBlock(4, 4, 4, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell56" name="cell56" onblur="checkInput(4, 5, 4, this.value, this.id)"  placeholder="3" disabled="disabled">
                                    </TD>
                                </TR>
                                
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell64" name="cell64" onblur="checkInput(5, 3, 4, this.value, this.id)" onclick="resetBlock(5, 3, 4, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell65" name="cell65" onblur="checkInput(5, 4, 4, this.value, this.id)"  placeholder="2" disabled="disabled">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell66" name="cell66" onblur="checkInput(5, 5, 4, this.value, this.id)" onclick="resetBlock(5, 5, 4, this.value, this.id)">
                                    </TD>
                                </TR>
                            </TABLE>
                        </TD>
                        <TD>
                            <TABLE>
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell47" name="cell47" onblur="checkInput(3, 6, 5, this.value, this.id)" onclick="resetBlock(3, 6, 5, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell48" name="cell48" onblur="checkInput(3, 7, 5, this.value, this.id)" onclick="resetBlock(3, 7, 5, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell49" name="cell49" onblur="checkInput(3, 8, 5, this.value, this.id)"  placeholder="3" disabled="disabled">
                                    </TD>
                                </TR>
                                
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell57" name="cell57" onblur="checkInput(4, 6, 5, this.value, this.id)" onclick="resetBlock(4, 6, 5, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell58" name="cell58" onblur="checkInput(4, 7, 5, this.value, this.id)" onclick="resetBlock(4, 7, 5, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell59" name="cell59" onblur="checkInput(4, 8, 5, this.value, this.id)"  placeholder="1" disabled="disabled">
                                    </TD>
                                </TR>
                                
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell67" name="cell67" onblur="checkInput(5, 6, 5, this.value, this.id)" onclick="resetBlock(5, 6, 5, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell68" name="cell68" onblur="checkInput(5, 7, 5, this.value, this.id)" onclick="resetBlock(5, 7, 5, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell69" name="cell69" onblur="checkInput(5, 8, 5, this.value, this.id)"  placeholder="6" disabled="disabled">
                                    </TD>
                                </TR>
                            </TABLE>
                        </TD>
                    </TR>
                    
                    <TR>
                        <TD>
                            <TABLE>
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell71" name="cell71" onblur="checkInput(6, 0, 6, this.value, this.id)" onclick="resetBlock(6, 0, 6, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell72" name="cell72" onblur="checkInput(6, 1, 6, this.value, this.id)"  placeholder="6" disabled="disabled">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell73" name="cell73" onblur="checkInput(6, 2, 6, this.value, this.id)" onclick="resetBlock(6, 2, 6, this.value, this.id)">
                                    </TD>
                                </TR>
                                
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell81" name="cell81" onblur="checkInput(7, 0, 6, this.value, this.id)" onclick="resetBlock(7, 0, 6, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell82" name="cell82" onblur="checkInput(7, 1, 6, this.value, this.id)" onclick="resetBlock(7, 1, 6, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell83" name="cell83" onblur="checkInput(7, 2, 6, this.value, this.id)" onclick="resetBlock(7, 2, 6, this.value, this.id)">
                                    </TD>
                                </TR>
                                
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell91" name="cell91" onblur="checkInput(8, 0, 6, this.value, this.id)" onclick="resetBlock(8, 0, 6, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell92" name="cell92" onblur="checkInput(8, 1, 6, this.value, this.id)" onclick="resetBlock(8, 1, 6, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell93" name="cell93" onblur="checkInput(8, 2, 6, this.value, this.id)" onclick="resetBlock(8, 2, 6, this.value, this.id)">
                                    </TD>
                                </TR>
                            </TABLE>
                        </TD>
                        <TD>
                            <TABLE>
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell74" name="cell74" onblur="checkInput(6, 3, 7, this.value, this.id)" onclick="resetBlock(6, 3, 7, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell75" name="cell75" onblur="checkInput(6, 4, 7, this.value, this.id)" onclick="resetBlock(6, 4, 7, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell76" name="cell76" onblur="checkInput(6, 5, 7, this.value, this.id)" onclick="resetBlock(6, 5, 7, this.value, this.id)">
                                    </TD>
                                </TR>
                                
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell84" name="cell84" onblur="checkInput(7, 3, 7, this.value, this.id)"  placeholder="4" disabled="disabled">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell85" name="cell85" onblur="checkInput(7, 4, 7, this.value, this.id)"  placeholder="1" disabled="disabled">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell86" name="cell86" onblur="checkInput(7, 5, 7, this.value, this.id)"  placeholder="9" disabled="disabled">
                                    </TD>
                                </TR>
                                
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell94" name="cell94" onblur="checkInput(8, 3, 7, this.value, this.id)" onclick="resetBlock(8, 3, 7, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell95" name="cell95" onblur="checkInput(8, 4, 7, this.value, this.id)"  placeholder="8" disabled="disabled">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell96" name="cell96" onblur="checkInput(8, 5, 7, this.value, this.id)" onclick="resetBlock(8, 5, 7, this.value, this.id)">
                                    </TD>
                                </TR>
                            </TABLE>
                        </TD>
                        <TD>
                            <TABLE>
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell77" name="cell77" onblur="checkInput(6, 6, 8, this.value, this.id)"  placeholder="2" disabled="disabled">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell78" name="cell78" onblur="checkInput(6, 7, 8, this.value, this.id)"  placeholder="8" disabled="disabled">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell79" name="cell79" onblur="checkInput(6, 8, 8, this.value, this.id)" onclick="resetBlock(6, 8, 8, this.value, this.id)">
                                    </TD>
                                </TR>
                                
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell87" name="cell87" onblur="checkInput(7, 6, 8, this.value, this.id)" onclick="resetBlock(7, 6, 8, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell88" name="cell88" onblur="checkInput(7, 7, 8, this.value, this.id)" onclick="resetBlock(7, 7, 8, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell89" name="cell89" onblur="checkInput(7, 8, 8, this.value, this.id)"  placeholder="5" disabled="disabled">
                                    </TD>
                                </TR>
                                
                                <TR>
                                    <TD>
                                        <input  type="text" id="cell97" name="cell97" onblur="checkInput(8, 6, 8, this.value, this.id)" onclick="resetBlock(8, 6, 8, this.value, this.id)">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell98" name="cell98" onblur="checkInput(8, 7, 8, this.value, this.id)"  placeholder="7" disabled="disabled">
                                    </TD>
                                    
                                     <TD>
                                         <input  type="text" id="cell99" name="cell99" onblur="checkInput(8, 8, 8, this.value, this.id)"  placeholder="9" disabled="disabled">
                                    </TD>
                                </TR>
                            </TABLE>
                        </TD>
                    </TR>
                </TABLE>
                
                <br>
                <br>
                <br>
                
                <DIV style="width: 5%;
                margin: 0 auto;">
                    <BUTTON onclick="refreshWindow()">
                        RESET
                    </BUTTON>
                </DIV>
            </DIV>
            
            <SCRIPT>
                
                // initialize required arrays to store entries in a particular row, colummn and block
                let rows = new Array(9);
                let cols = new Array(9);
                let blocks = new Array(9);
                
                
                // set the initial board state
                rows[0] = new Set([3, 5, 7]);
                rows[1] = new Set([1, 5, 6, 9]);
                rows[2] = new Set([6, 8, 9]);
                rows[3] = new Set([3, 6, 8]);
                rows[4] = new Set([1, 3, 4, 8]);
                rows[5] = new Set([2, 6, 7]);
                rows[6] = new Set([2, 6, 8]);
                rows[7] = new Set([1, 4, 5, 9]);
                rows[8] = new Set([7, 8, 9]);
                
                cols[0] = new Set([5,6, 8, 4, 7]);
                cols[1] = new Set([3, 9, 6]);
                cols[2] = new Set([8]);
                cols[3] = new Set([1, 4, 8]);
                cols[4] = new Set([7, 9, 6, 2, 1, 8]);
                cols[5] = new Set([5, 3, 9]);
                cols[6] = new Set([2]);
                cols[7] = new Set([6, 8, 7]);
                cols[8] = new Set([1, 3, 6, 5, 9]);
                
                blocks[0] = new Set([3, 5, 6, 8, 9]);
                blocks[1] = new Set([1, 7, 9, 5]);
                blocks[2] = new Set([6]);
                blocks[3] = new Set([8, 4, 7]);
                blocks[4] = new Set([8,6, 3, 2]);
                blocks[5] = new Set([1, 3, 6]);
                blocks[6] = new Set([6]);
                blocks[7] = new Set([1, 4, 9, 8]);
                blocks[8] = new Set([2, 8, 5, 7, 9]);

                let allowed_inputs = new Set([1, 2, 3, 4, 5, 6, 7, 8, 9]);
                
                // this function refreshes and resets the state of the game
                function refreshWindow() {
                    window.location.reload();
                }
                
                // this function resets the value in any block where the user wishes to change the entered value
                function resetBlock(row_number, col_number, block_number, input, id) {
                    rows[row_number].delete(Number(input));
                    cols[col_number].delete(Number(input));
                    blocks[block_number].delete(Number(input));
                    document.getElementById(id).removeAttribute("disabled");
                    document.getElementById(id).focus();
                    //document.getElementById(id).value = "";
                    document.getElementById(id).style.backgroundColor = "white";
                }
                
                // this function validates the user input against the game rules
                function checkInput(row_number, col_number, block_number, input, id) {
                    console.log(!allowed_inputs.has(Number(input)));
                    
                    if(!allowed_inputs.has(Number(input)) && input != "") {
                        document.getElementById(id).focus();
                        document.getElementById(id).value = "";
                        alert("Please enter a number from 1 to 9!")
                        return;
                    }
                    
                    if(input != "" && !rows[row_number].has(Number(input)) && !cols[col_number].has(Number(input)) && !blocks[block_number].has(Number(input))) {
                        console.log(true);
                        rows[row_number].add(Number(input));
                        cols[col_number].add(Number(input));
                        blocks[block_number].add(Number(input));
                        document.getElementById(id).style.backgroundColor = "#78AB46";
                    }
                    else if(input != ""){
                        document.getElementById(id).focus();
                        document.getElementById(id).value = ""; 
                        alert(input + " cannot be placed at row: " + Number(row_number+1) + " and column: " + Number(col_number+1));
                        return;
                    }
                    
                    if(checkFinalState()) {
                        alert("Congratulations!! Puzzle solved successfully!");
                        return;
                    }
                }
                
                
                // this function checks if the finish state of the game is reached
                function checkFinalState() {
                    for(var i = 0; i < 9; i++) {
                        if(rows[i].size != 9) {
                            return false;
                        }
                    }
                    return true;
                }
            </SCRIPT>
        </BODY>
</HTML>
