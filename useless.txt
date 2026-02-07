//Problem-01: New Price for Eid Sale
function newPrice(currentPrice, discount) {
    if(typeof(currentPrice) === "string" || typeof(discount) === "string"){
        return "Invalid";
    }
    let res = currentPrice - ((discount/100)* currentPrice);
    return res.toFixed(3);
}

//Problem-02: OTP Validation for Zapshift
function validOtp(otp) {
    // Your code here
    if(typeof(otp) != "string" ){
        return "Invalid";
    }
    if(!otp.startsWith("ph-") || otp.length != 8){
        return false;
    }
    return true;
}

//Problem-03: BCS Final Score Calculator
function finalScore(omr) {
    //write your code here
    if(omr.right + omr.wrong + omr.skip != 100){
        return "Invalid";
    }
    let score = omr.right - (omr.wrong * 0.5);
    return Math.round(score);
}

//Problem-04: Upcoming Gono Vote
function gonoVote(array) {
    //write your code here
    if(!Array.isArray(array)) return "Invalid";
    let ha = 0;
    let na = 0;
    for(let x of array){
        if(x == "ha") ha++;
        else na++;
    }
    if(ha > na) return true;
    else if(na > ha) return false;

    return "equal";
}

//Problem-05: Text Analyzer for an AI Company
function analyzeText(str) {

    if (typeof (str) != "string" || str.length === 0) return "Invalid";

    const arr = str.split(" ");
    let count = 0;
    let maxWord = "";
    for (let s of arr) {
        if (s.length > maxWord.length) {
            maxWord = s;
        }
        count += s.length;
    }
    return {
        longwords: maxWord,   
        token: count  
    };

}

