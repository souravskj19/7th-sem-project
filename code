<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-rbsA2VBKQhggwzxH7pPCaAqO46MgnOM80zW1RWuH61DGLwZJEdK2Kadq2F9CUG65" crossorigin="anonymous">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.2/font/bootstrap-icons.css">
    <title>Fee Management System</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #ecf0f1;
        }
        .navbar {
            background-color: #3498db;
        }
        .card {
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
            background-color: #f7f7f7;
        }
        .card-title {
            font-weight: bold;
            font-size: 18px;
            color: #2ecc71;
        }
        .table {
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
        }
        .modal-content {
            border-radius: 10px;
            background-color: #f7f7f7;
        }
        .btn {
            border-radius: 10px;
        }
        .btn-primary {
            background-color: #3498db;
            border-color: #3498db;
        }
        .btn-success {
            background-color: #2ecc71;
            border-color: #2ecc71;
        }
        .btn-danger {
            background-color: #e74c3c;
            border-color: #e74c3c;
        }
        .btn-warning {
            background-color: #ffc107;
            border-color: #ffc107;
        }
        .btn-info {
            background-color: #9b59b6;
            border-color: #9b59b6;
        }
        .student-image {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            border: 2px solid #f1c40f;
        }
        .total-fee {
            color: #e74c3c;
        }
        .total-paid {
            color: #2ecc71;
        }
        .total-due {
            color: #ffc107;
        }
    </style>
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
        <div class="container-fluid">
            <a class="navbar-brand" href="#" style="color: #fff;">Fee Management System</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#" id="dashboard-link" style="color: #fff;">Dashboard</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#" id="students-link" style="color: #fff;">Students</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#" id="payments-link" style="color: #fff;">Payments</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#" id="reports-link" style="color: #fff;">Reports</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
    <div class="container mt-5">
        <div class="row">
            <div class="col-md-4">
                <div class="card p-3">
                    <div class="card-body">
                        <h5 class="card-title">Total Fee: <span class="total-fee" id="total-fee">$0</span></h5>
                        <h5 class="card-title">Total Paid: <span class="total-paid" id="total-paid">$0</span></h5>
                        <h5 class="card-title">Total Due: <span class="total-due" id="total-due">$0</span></h5>
                        <img src="https://via.placeholder.com/100" class="student-image" alt="Student Image">
                    </div>
                </div>
            </div>
            <div class="col-md-8">
                <button type="button" class="btn btn-success mb-3" data-bs-toggle="modal" data-bs-target="#addStudentModal">
                    <i class="bi bi-person-plus"></i> Add Student
                </button>
                <table class="table table-striped table-hover">
                    <thead class="table-dark">
                        <tr>
                            <th scope="col">Image</th>
                            <th scope="col">Name</th>
                            <th scope="col">Fee</th>
                            <th scope="col">Paid</th>
                            <th scope="col">Due</th>
                            <th scope="col">Action</th>
                        </tr>
                    </thead>
                    <tbody id="student-table-body">
                    </tbody>
                </table>
            </div>
        </div>
    </div>
    <div class="modal fade" id="addStudentModal" tabindex="-1" aria-labelledby="addStudentModalLabel" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="addStudentModalLabel">Add Student</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <form id="add-student-form" enctype="multipart/form-data">
                        <div class="mb-3">
                            <label for="name" class="form-label">Name</label>
                            <input type="text" class="form-control" id="name" name="name" required>
                        </div>
                        <div class="mb-3">
                            <label for="fee" class="form-label">Fee</label>
                            <input type="number" class="form-control" id="fee" name="fee" required>
                        </div>
                        <div class="mb-3">
                            <label for="paid" class="form-label">Paid</label>
                            <input type="number" class="form-control" id="paid" name="paid" required>
                        </div>
                        <div class="mb-3">
                            <label for="image" class="form-label">Image</label>
                            <input type="file" class="form-control" id="image" name="image" accept="image/*">
                        </div>
                        <button type="submit" class="btn btn-primary">Add Student</button>
                    </form>
                </div>
            </div>
        </div>
    </div>
    <div class="modal fade" id="updateStudentModal" tabindex="-1" aria-labelledby="updateStudentModalLabel" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="updateStudentModalLabel">Update Student</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <form id="update-student-form" enctype="multipart/form-data">
                        <input type="hidden" id="update-student-id" name="id">
                        <div class="mb-3">
                            <label for="update-name" class="form-label">Name</label>
                            <input type="text" class="form-control" id="update-name" name="name" required>
                        </div>
                        <div class="mb-3">
                            <label for="update-fee" class="form-label">Fee</label>
                            <input type="number" class="form-control" id="update-fee" name="fee" required>
                        </div>
                        <div class="mb-3">
                            <label for="update-paid" class="form-label">Paid</label>
                            <input type="number" class="form-control" id="update-paid" name="paid" required>
                        </div>
                        <div class="mb-3">
                            <label for="update-image" class="form-label">Image</label>
                            <input type="file" class="form-control" id="update-image" name="image" accept="image/*">
                        </div>
                        <button type="submit" class="btn btn-primary">Update Student</button>
                    </form>
                </div>
            </div>
        </div>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-kenU1KFdBIe4zVF0s0G1M5b4hcpxyD9F7jL+jjXkk+Q2h455rYXK/7HAuoJl+0I4" crossorigin="anonymous"></script>
    <script>
        let students = [];

        document.getElementById('add-student-form').addEventListener('submit', (e) => {
            e.preventDefault();
            const name = document.getElementById('name').value;
            const fee = parseInt(document.getElementById('fee').value);
            const paid = parseInt(document.getElementById('paid').value);
            const due = fee - paid;
            const image = document.getElementById('image').files[0];
            const reader = new FileReader();
            reader.onload = () => {
                students.push({ name, fee, paid, due, image: reader.result });
                updateDashboard();
                updateStudentTable();
                document.getElementById('add-student-form').reset();
                const addStudentModal = document.getElementById('addStudentModal');
                const modal = bootstrap.Modal.getInstance(addStudentModal);
                modal.hide();
            };
            reader.readAsDataURL(image);
        });

        function updateDashboard() {
            const totalFee = students.reduce((acc, student) => acc + student.fee, 0);
            const totalPaid = students.reduce((acc, student) => acc + student.paid, 0);
            const totalDue = students.reduce((acc, student) => acc + student.due, 0);
            document.getElementById('total-fee').innerText = totalFee;
            document.getElementById('total-paid').innerText = totalPaid;
            document.getElementById('total-due').innerText = totalDue;
        }

        function updateStudentTable() {
            const studentTableBody = document.getElementById('student-table-body');
            studentTableBody.innerHTML = '';
            students.forEach((student, index) => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td><img src="${student.image}" class="student-image" alt="Student Image"></td>
                    <td>${student.name}</td>
                    <td>$${student.fee}</td>
                    <td>$${student.paid}</td>
                    <td>$${student.due}</td>
                    <td>
                        <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#updateStudentModal" onclick="fillUpdateForm(${index})">
                            <i class="bi bi-pencil-square"></i> Update
                        </button>
                        <button type="button" class="btn btn-danger" onclick="deleteStudent(${index})">
                            <i class="bi bi-trash"></i> Delete
                        </button>
                    </td>
                `;
                studentTableBody.appendChild(row);
            });
        }

        function fillUpdateForm(index) {
            const student = students[index];
            document.getElementById('update-student-id').value = index;
            document.getElementById('update-name').value = student.name;
            document.getElementById('update-fee').value = student.fee;
            document.getElementById('update-paid').value = student.paid;
            const updateImage = document.getElementById('update-image');
            const reader = new FileReader();
            reader.onload = () => {
                updateImage.setAttribute('data-image', reader.result);
            };
            reader.readAsDataURL(new Blob([student.image], { type: 'image/jpeg' }));
        }

        document.getElementById('update-student-form').addEventListener('submit', (e) => {
            e.preventDefault();
            const index = parseInt(document.getElementById('update-student-id').value);
            const name = document.getElementById('update-name').value;
            const fee = parseInt(document.getElementById('update-fee').value);
            const paid = parseInt(document.getElementById('update-paid').value);
            const due = fee - paid;
            const image = document.getElementById('update-image').files[0];
            if (image) {
                const reader = new FileReader();
                reader.onload = () => {
                    students[index] = { name, fee, paid, due, image: reader.result };
                    updateDashboard();
                    updateStudentTable();
                    const updateStudentModal = document.getElementById('updateStudentModal');
                    const modal = bootstrap.Modal.getInstance(updateStudentModal);
                    modal.hide();
                };
                reader.readAsDataURL(image);
            } else {
                students[index] = { name, fee, paid, due, image: students[index].image };
                updateDashboard();
                updateStudentTable();
                const updateStudentModal = document.getElementById('updateStudentModal');
                const modal = bootstrap.Modal.getInstance(updateStudentModal);
                modal.hide();
            }
        });

        function deleteStudent(index) {
            students.splice(index, 1);
            updateDashboard();
            updateStudentTable();
        }
    </script>
</body>
</html>
