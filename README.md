### Learn Typescript

<details>
  <summary>Tài liệu tham khảo</summary>
  <ul>
    <li><a href="https://www.youtube.com/playlist?list=PLncHg6Kn2JT5emvXmG6kgeGkrQjRqxsb4">Full playlist here</a></li>
    <li><a href="https://drive.google.com/file/d/1fSByxnd8dHwaCM48zmh80iSRObVx2xin/view">Document</a></li>
    <li><a href="https://www.youtube.com/watch?v=E6k6R4PnLV0">How to install NVM on Windows 11</a></li>
  </ul>
</details>

#### 4 Why TypeScript

TS với hệ thống

Types => hạn chế bugs khi khối lượng codebase lớn (các project lớn, nhiều members)

##### 4.1. Dynamic types với javascript

- Javascript là ngôn ngữ với 'type' động, có nghĩa là chúng ta có thể thay đổi "datatype" - kiểu dữ liệu
- Ví dụ:

```Typescript
let name = 'abc'; typeof === string
name = 35; typeof === number
name = false; typeof === boolean
```

- Dynamic types (type động) mang tới sự freedom, tuy nhiên, tự do quá thì...

##### 4.2. Vấn đề với Dynamic types

- Cho ra sai kết quả (nếu truyền vào sai type) => cần code bổ sung validate => typescript sinh ra để khắc phục nhược điểm trên.

#### 5 TypeScript Types

##### 5.1. Type là gì ?

Type gồm 2 loại:
keyword 'type' và data-types (kiểu dữ liệu)

Ở đây, chúng ta sẽ đề cập tới 'data-types: kiểu dữ liệu
Việc định nghĩa kiểu dữ liệu (data-types), sẽ nói cho chúng ta biết,
biến số (variable) có những thuộc tính và functions nào

Ví dụ:

```Typescript
const name = "Hello";
```

Khi nhìn vào value 'Hello', chúng ta sẽ nghĩ nó là string. (data-type === String)

Một vài thuộc tính và function của string:

```Typescript
console.log('Hello'.length); //5 => property: length (có thuộc tính length)
console.log('Hello'.toUpperCase()); // HELLO => có functions
```

=> dựa vào type (data-types), trình compiler sẽ biết được 1 tham số (variable/value)
sẽ có những thuộc tính (property) và phương thức (functions) nào.

##### 5.2. Các loại data-types với Typescript

Tương tự như javascript, TS datatype bao gồm:

- Dữ liệu nguyên thủy
- Dữ liệu tham chiếu

- Primitive data- types:
  String, number, boolean, null, undefined, symbol, bigint

- References dataTypes: Objects, Array, Functions..

#### 6. Type Annotations - Keyword Type

##### 6.1. Cú pháp và đặc điểm

TypeScript sử dụng cú pháp `:type` sau khi định nghĩa biến để khai báo kiểu dữ liệu (type) cho biến đó. Khi đã khai báo type, bạn không thể thay đổi kiểu dữ liệu của biến (tính chất static type).

###### Ví dụ:

- Khai báo biến và định nghĩa kiểu dữ liệu, nhưng chưa khởi tạo giá trị:

```typescript
let variableName: type;
```

- Khai báo biến, định nghĩa kiểu dữ liệu và gán giá trị khởi tạo:

```typescript
let variableName: type = value;
```

- Khai báo hằng số, định nghĩa kiểu dữ liệu và gán giá trị khởi tạo:

```typescript
const constantName: type = value;
```

##### 6.2. Ứng dụng với kiểu dữ liệu nguyên thủy (Primitive data types)

###### Ví dụ:

```typescript
let count: number; // Khai báo biến `count` kiểu number

count = 1; // Gán giá trị 1 (kiểu number) cho biến `count` thành công

count = "name"; // Gán giá trị "name" (kiểu string) cho biến `count` báo lỗi

// Khai báo biến `count` kiểu number và khởi tạo giá trị ban đầu là 1
let count: number = 1;
```

##### 6.3. Ứng dụng với kiểu dữ liệu tham chiếu (Reference data types)

###### Ví dụ:

```typescript
let arrayName: type[]; // Khai báo biến `arrayName` là mảng kiểu `type`

// Ví dụ cụ thể:
let names: string[] = ["a", "b", "c"]; // Khai báo mảng `names` chỉ chứa các phần tử kiểu string

names.push(1); // Gán giá trị 1 (kiểu number) cho mảng `names` báo lỗi
```

###### Lưu ý:

- Sử dụng `[]` sau kiểu dữ liệu để biểu thị mảng.
- Kiểu dữ liệu trong ngoặc vuông chỉ ra kiểu dữ liệu của các phần tử trong mảng.

##### 6.4. Một số ví dụ nâng cao

- Khai báo biến `person` là object có hai thuộc tính `name` (kiểu string) và `age` (kiểu number):

```typescript
let person: { name: string; age: number };

person = { name: "John Doe", age: 30 };
```

###### Tóm tắt

- Keyword Type cho phép khai báo kiểu dữ liệu cho biến, giúp tăng tính an toàn và bảo mật cho code.
- TypeScript hỗ trợ nhiều kiểu dữ liệu đa dạng, bao gồm cả kiểu dữ liệu nguyên thủy và kiểu dữ liệu tham chiếu.
- Sử dụng cú pháp và quy tắc phù hợp để khai báo các biến với kiểu dữ liệu mong muốn.
