<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Регистрация на курс</title>

    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #111827, #1e293b);
            color: #fff;
            min-height: 100vh;
            padding: 40px 20px;
        }

        .container {
            max-width: 950px;
            margin: auto;
        }

        /* Заголовок */

        .header {
            text-align: center;
            margin-bottom: 35px;
        }

        .header h1 {
            font-size: 42px;
            margin-bottom: 10px;
        }

        .header p {
            color: #aeb8c7;
            font-size: 18px;
        }

        /* Карточка */

        .card {
            background: #ffffff;
            color: #222;
            border-radius: 20px;
            padding: 35px;
            box-shadow: 0 20px 50px rgba(0,0,0,0.35);
            margin-bottom: 30px;
        }

        .card h2 {
            color: #2563eb;
            margin-bottom: 25px;
            font-size: 26px;
        }

        /* Форма */

        .form-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        .form-group {
            display: flex;
            flex-direction: column;
        }

        .full {
            grid-column: 1 / 3;
        }

        label {
            font-weight: bold;
            margin-bottom: 8px;
            color: #374151;
        }

        .required {
            color: #ef4444;
        }

        input,
        select,
        textarea {
            width: 100%;
            padding: 13px 15px;
            border: 2px solid #e5e7eb;
            border-radius: 10px;
            font-size: 16px;
            outline: none;
            transition: 0.3s;
            background: #f9fafb;
        }

        input:focus,
        select:focus,
        textarea:focus {
            border-color: #2563eb;
            background: white;
            box-shadow: 0 0 0 3px rgba(37,99,235,0.12);
        }

        textarea {
            min-height: 120px;
            resize: vertical;
        }

        /* Checkbox */

        .agreement {
            grid-column: 1 / 3;
            display: flex;
            align-items: center;
            gap: 10px;
            margin-top: 5px;
        }

        .agreement input {
            width: 18px;
            height: 18px;
            cursor: pointer;
        }

        .agreement label {
            margin: 0;
            font-weight: normal;
        }

        /* Кнопка */

        .submit-button {
            grid-column: 1 / 3;
        }

        button {
            width: 100%;
            border: none;
            padding: 15px;
            border-radius: 10px;
            background: linear-gradient(135deg, #2563eb, #4f46e5);
            color: white;
            font-size: 18px;
            font-weight: bold;
            cursor: pointer;
            transition: 0.3s;
        }

        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(37,99,235,0.35);
        }

        /* Таблица */

        .schedule-card {
            background: #ffffff;
            color: #222;
            border-radius: 20px;
            padding: 35px;
            box-shadow: 0 20px 50px rgba(0,0,0,0.35);
        }

        .schedule-card h2 {
            color: #2563eb;
            margin-bottom: 20px;
        }

        .table-wrapper {
            overflow-x: auto;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            overflow: hidden;
            border-radius: 10px;
        }

        th {
            background: #2563eb;
            color: white;
            padding: 15px;
            text-align: left;
        }

        td {
            padding: 14px 15px;
            border-bottom: 1px solid #e5e7eb;
        }

        tr:nth-child(even) {
            background: #f8fafc;
        }

        tr:hover {
            background: #eef4ff;
        }

        /* Низ */

        .footer {
            text-align: center;
            color: #94a3b8;
            margin-top: 25px;
            font-size: 14px;
        }

        /* Телефон */

        @media (max-width: 650px) {

            body {
                padding: 20px 10px;
            }

            .header h1 {
                font-size: 30px;
            }

            .card,
            .schedule-card {
                padding: 20px;
            }

            .form-grid {
                grid-template-columns: 1fr;
            }

            .full,
            .agreement,
            .submit-button {
                grid-column: 1;
            }

            table {
                font-size: 14px;
            }

            th,
            td {
                padding: 10px;
            }
        }
    </style>
</head>

<body>

<div class="container">

    <!-- Заголовок -->

    <div class="header">
        <h1>🎓 Регистрация на курс</h1>
        <p>Заполните форму, чтобы записаться на обучение</p>
    </div>


    <!-- Форма -->

    <div class="card">

        <h2>📝 Данные участника</h2>

        <form>

            <div class="form-grid">

                <!-- Имя -->

                <div class="form-group">
                    <label for="name">
                        Имя <span class="required">*</span>
                    </label>

                    <input
                        type="text"
                        id="name"
                        name="name"
                        placeholder="Введите имя"
                        required
                    >
                </div>


                <!-- Фамилия -->

                <div class="form-group">
                    <label for="surname">
                        Фамилия <span class="required">*</span>
                    </label>

                    <input
                        type="text"
                        id="surname"
                        name="surname"
                        placeholder="Введите фамилию"
                        required
                    >
                </div>


                <!-- Email -->

                <div class="form-group">
                    <label for="email">
                        Email <span class="required">*</span>
                    </label>

                    <input
                        type="email"
                        id="email"
                        name="email"
                        placeholder="example@mail.com"
                        required
                    >
                </div>


                <!-- Телефон -->

                <div class="form-group">
                    <label for="phone">
                        Телефон <span class="required">*</span>
                    </label>

                    <input
                        type="tel"
                        id="phone"
                        name="phone"
                        placeholder="+996 XXX XXX XXX"
                        required
                    >
                </div>


                <!-- Возраст -->

                <div class="form-group">
                    <label for="age">
                        Возраст
                    </label>

                    <input
                        type="number"
                        id="age"
                        name="age"
                        min="5"
                        max="100"
                        placeholder="Ваш возраст"
                    >
                </div>


                <!-- Направление -->

                <div class="form-group">
                    <label for="direction">
                        Направление обучения
                    </label>

                    <select id="direction" name="direction">

                        <option value="">
                            Выберите направление
                        </option>

                        <option value="html">
                            HTML и CSS
                        </option>

                        <option value="javascript">
                            JavaScript
                        </option>

                        <option value="python">
                            Python
                        </option>

                        <option value="web">
                            Web-разработка
                        </option>

                        <option value="design">
                            Web-дизайн
                        </option>

                    </select>
                </div>


                <!-- Формат -->

                <div class="form-group">
                    <label for="format">
                        Формат обучения <span class="required">*</span>
                    </label>

                    <select
                        id="format"
                        name="format"
                        required
                    >

                        <option value="">
                            Выберите формат
                        </option>

                        <option value="online">
                            💻 Онлайн
                        </option>

                        <option value="offline">
                            🏫 Очно
                        </option>

                    </select>
                </div>


                <!-- Комментарий -->

                <div class="form-group full">

                    <label for="comment">
                        Комментарий
                    </label>

                    <textarea
                        id="comment"
                        name="comment"
                        placeholder="Напишите ваш комментарий..."
                    ></textarea>

                </div>


                <!-- Согласие -->

                <div class="agreement">

                    <input
                        type="checkbox"
                        id="agreement"
                        name="agreement"
                        required
                    >

                    <label for="agreement">
                        Я согласен(на) с условиями регистрации
                        <span class="required">*</span>
                    </label>

                </div>


                <!-- Кнопка -->

                <div class="submit-button">

                    <button type="submit">
                        🚀 Отправить заявку
                    </button>

                </div>

            </div>

        </form>

    </div>


    <!-- Расписание -->

    <div class="schedule-card">

        <h2>📅 Расписание курса</h2>

        <div class="table-wrapper">

            <table>

                <thead>

                    <tr>
                        <th>День</th>
                        <th>Время</th>
                        <th>Тема</th>
                        <th>Преподаватель</th>
                    </tr>

                </thead>

                <tbody>

                    <tbody>

    <tr>
        <td>Понедельник</td>
        <td>17:00–19:00</td>
        <td>Урок 3</td>
        <td>Феликс Мардонкудов</td>
    </tr>

    <tr>
        <td>Четверг</td>
        <td>17:00–19:00</td>
        <td>HTML и CSS</td>
        <td>Феликс Мардонкудов</td>
    </tr>

</tbody>
                </tbody>

            </table>

        </div>

    </div>


    <div class="footer">
        © 2026 Регистрация на курс
    </div>

</div>

</body>
</html>
