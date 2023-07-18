
function generateMealPlanPage() {
    var name= document.getElementById("name").value;
    var email= document.getElementById("email").value;
    var goal= document.getElementById("goal").value;

    if(!isValidEmail(email)){
        alert("Invalid email. Please enter a valid email address.");
        return;
    }
    var days= ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday'];
var mealPlan= [];
for (var i=0; i< days.length; i++){
    var meals= {
        breakfast: document.getElementById(days[i]+'-breakfast').value,
        snack1: document.getElementById(days[i]+'-snack#1').value,
        lunch: document.getElementById(days[i]+'-lunch').value,
        snack2: document.getElementById(days[i]+'-snack#2').value,
        dinner: document.getElementById(days[i]+'-dinner').value
    };
    mealPlan.push({day: days[i], meals:meals});
}
 var mealPlanContent=`<!DOCTYPE html>
    <html>
    <head>
        <title>Weekly Meal Plan</title>
        <link rel="stylesheet" type="text/css" href="final.css">
    </head>
    <body>
        <h1>Weekly Meal Plan</h1>
        <p><strong>Name:</strong> ${name}</p>
        <p><strong>Email:</strong> ${email}</p>
        <p><strong>Goal for the Week:</strong> ${goal}</p>
        <table>
            <thead>
                <tr>
                    <th></th>
                    <th>Monday</th>
                    <th>Tuesday</th>
                    <th>Wednesday</th>
                    <th>Thursday</th>
                    <th>Friday</th>
                    <th>Saturday</th>
                    <th>Sunday</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <th>Breakfast</th>
                    ${generateMealPlanRow(mealPlan, 'breakfast')}
                </tr>
                <tr>
                    <th>Snack #1</th>
                    ${generateMealPlanRow(mealPlan, 'snack1')}
                </tr>
                <tr>
                    <th>Lunch</th>
                    ${generateMealPlanRow(mealPlan, 'lunch')}
                </tr>
                <tr>
                    <th>Snack #2</th>
                    ${generateMealPlanRow(mealPlan, 'snack2')}
                </tr>
                <tr>
                    <th>Dinner</th>
                    ${generateMealPlanRow(mealPlan, 'dinner')}
                </tr>
            </tbody>
        </table>
    </body>
    </html>`;

    var mealPlanPage = document.createElement('div');
    mealPlanPage.innerHTML = mealPlanContent;

    document.body.appendChild(mealPlanPage);
}
function generateMealPlanRow(mealPlan, mealType) {


}

function clearTable(){

    const table= document.getElementById("mealPlanContent");

    table.innerHTML ="";
}
document.getElementById("clear-btn").addEventListener("click", clearTable);
document.getElementById("create-btn").addEventListener("click", generateMealPlanPage);