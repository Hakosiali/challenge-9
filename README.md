# challenge-9
function averageOfEvenNumbers(numbers) {
  const evenNumbers = numbers.filter(num => num % 2 === 0);
  const sum = evenNumbers.reduce((acc, num) => acc + num, 0);
  return evenNumbers.length > 0 ? sum / evenNumbers.length : 0;
}
function longestWord(words) {
  return words.reduce((longest, current) => (current.length > longest.length ? current : longest), '');
}
function averagePagesInBooks(books) {
  const totalPages = books.map(book => book.pages).reduce((acc, pages) => acc + pages, 0);
  return books.length > 0 ? totalPages / books.length : 0;
}
function stringFrequency(strings) {
  return strings.reduce((freqObj, str) => {
    freqObj[str] = (freqObj[str] || 0) + 1;
    return freqObj;
  }, {});
}
function countPeopleByCity(people) {
  return people.reduce((cityCount, person) => {
    const { city } = person;
    cityCount[city] = (cityCount[city] || 0) + 1;
    return cityCount;
  }, {});
}
const numbers = [1, 2, 3, 4, 5, 6];
console.log(averageOfEvenNumbers(numbers));

const words = ["apple", "banana", "grapefruit", "kiwi"];
console.log(longestWord(words));

const books = [
  { title: "Book 1", author: "Author 1", pages: 100 },
  { title: "Book 2", author: "Author 2", pages: 150 },
  { title: "Book 3", author: "Author 3", pages: 120 },
];
console.log(averagePagesInBooks(books));

const strings = ["hello", "world", "hello"];
console.log(stringFrequency(strings));

const people = [
  { name: "Alice", age: 30, city: "New York" },
  { name: "Bob", age: 40, city: "Chicago" },
  { name: "Charlie", age: 50, city: "New York" },
];
console.log(countPeopleByCity(people));

