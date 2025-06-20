<!DOCTYPE html>
<html>
<head>
    <title>myDog Output</title>
</head>
<body>
    <h1>Output from myDog and myDogConst</h1>
    <div id="output"></div>

    <script>
        // Your full JavaScript code goes here (from canvas)
        let myDog = {
            name: "Scooby-Doo",
            breed: "Great Dane",
            origin: "Scooby-Doo, Where Are You!",
            personality: "goofy and cowardly",
            mySound: "Ruh-roh! I’m Scooby-Doo! You might not be scared, but I am!",
            canTalk: true,
            myGreeting: function() {
                return `Hello, my name is ${this.name}, I am a ${this.breed} from the show '${this.origin}'. My personality is ${this.personality}, and I say: "${this.mySound}". Can I talk? ${this.canTalk}`;
            }
        };

        function Dog(name, breed, origin, personality, mySound, canTalk) {
            this.name = name;
            this.breed = breed;
            this.origin = origin;
            this.personality = personality;
            this.mySound = mySound;
            this.canTalk = canTalk;
            this.myGreeting = function() {
                return `Hello, my name is ${this.name}, I am a ${this.breed} from the show '${this.origin}'. My personality is ${this.personality}, and I say: "${this.mySound}". Can I talk? ${this.canTalk}`;
            };
        }

        let myDogConst = new Dog("Scooby-Doo", "Great Dane", "Scooby-Doo, Where Are You!", "goofy and cowardly", "Ruh-roh! I’m Scooby-Doo! You might not be scared, but I am!", true);

        // Output to page
        document.getElementById("output").innerHTML =
            `<p>${myDog.myGreeting()}</p><p>${myDogConst.myGreeting()}</p>`;
    </script>
</body>
</html>
