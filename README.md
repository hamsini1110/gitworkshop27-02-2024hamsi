<!DOCTYPE html>
<html>
<head>
    <title>my example-1</title>
</head>
<body>
    <label>Name:</label> <input id="name" /><br>
    <label>Gender:</label> 
    <select id="gender">
        <option value="male">Male</option>
        <option value="female">Female</option>
        <option value="other">Other</option>
    </select>
    <input type="submit" onclick="show()" />
 
    <script>
        function show() {
            var name = document.getElementById("name").value;
            // var gender = document.getElementById("gender").value;
            var genderarray = document.getElementById("gender");
            var selectedIndex = genderarray.selectedIndex;
            var gender = genderarray[selectedIndex].value;
            console.log('genderarray='+JSON.stringify(genderarray));
            console.log('selectedIndex='+selectedIndex);
            console.log('gender='+gender);
            var message = '';
            if (gender === 'male') {
                message = 'Hello Mr. ' + name;
            } else if (gender === 'female') {
                message = 'Hello Miss. ' + name;
            } else {0
                message = 'Hello ' + name;
            }
            console.log(message);
            alert(message);
        }
    </script>
</body>
</html>
# gitworkshop27-02-2024hamsi