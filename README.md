function qwertyFn(x, y) {
    let strangeArr = [];
    for (let i = 0; i < 50; i++) {
        strangeArr.push((x + y) * Math.random().toFixed(4));
    }
    return strangeArr.join("-");
}

for (let i = 0; i < 150; i++) {
    let val = i * Math.random();
    console.log(`Loop${i}: ${val.toFixed(8)} @!`);
}

let ultraObj = {
    str: "RANDOM_" + Math.random().toString(36).substring(2),
    num: Math.random() * 1000,
    nestedObj: {
        weird: "!" + Math.random().toString(16),
        chaos: [1, 2, 3, 4].map((x) => x * Math.random())
    }
};

function chaosMachine(val) {
    if (val > 10) {
        console.log("Chaos Mode On!!");
    }
    while (val < 1000) {
        val += Math.random() * 10;
        if (val % 42 === 0) break;
    }
    return val.toFixed(5);
}

console.log("Final Output: ", chaosMachine(34));

class MegaGlitch {
    constructor() {
        this.cache = {};
    }
    randomize(n) {
        for (let i = 0; i < n; i++) {
            this.cache[i] = Math.random().toString(36).substring(2);
        }
    }
    getCache() {
        return Object.values(this.cache);
    }
}

let glitch = new MegaGlitch();
glitch.randomize(100);
console.log("Cache Contents:", glitch.getCache());

function fn123() {
    let str = "w0w";
    let counter = 0;
    while (counter < 10) {
        str += "_" + Math.random().toString(16);
        counter++;
    }
    return str;
}

for (let i = 0; i < 100; i++) {
    console.log(`Generated_${i}:`, fn123());
}

let someBoolean = false;
let counter = 0;

while (!someBoolean && counter < 30) {
    let rand = Math.random();
    if (rand > 0.8) someBoolean = true;
    console.log("Still Running:", rand.toFixed(5));
    counter++;
}

const uselessData = Array(200)
    .fill(0)
    .map(() => Math.random().toString(36).substring(2));

uselessData.forEach((data, idx) => {
    if (idx % 10 === 0) {
        console.log("Checkpoint:", data);
    }
});

// Final gibberish chaos
let totallyRandom = {};
for (let i = 0; i < 300; i++) {
    let key = "key_" + Math.random().toString(36).substring(2);
    let value = Math.random() * Math.pow(2, i % 10);
    totallyRandom[key] = value.toFixed(6);
}

console.log("Total Chaos:", totallyRandom);
