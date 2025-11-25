===============================================
SUPABASE PORTFOLIO-BACKEND - КОНФИГУРАЦИЯ
===============================================
Дата создания: 25 ноября 2025

PROJECT ИНФОРМАЦИЯ:
-------------------
Project Name: Portfolio-Backend
Project ID: fsovbwvbhwcdqebbxwdn
Region: Central EU (Frankfurt) - eu-central-1
Database Password: SuperStrongPass2025!

API CREDENTIALS:
----------------
Project URL: https://fsovbwvbhwcdqebbxwdn.supabase.co

Anon Public Key:
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6ImZzb3Zid3ZiaHdjZHFlYmJ4d2RuIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NjQwODc3ODgsImV4cCI6MjA3OTY2Mzc4OH0.QH3E4GVvcDzKdZAbLCw2MqcOqHmPVONZ_SwdECmdY08

DATABASE SCHEMA:
----------------
Таблица: contacts
Поля:
  - id: bigint (primary key, auto-increment)
  - created_at: timestamp with time zone (default: now())
  - name: text (not null)
  - email: text (not null)
  - message: text (not null)

Security:
  - Row Level Security: ENABLED
  - Policy: "Allow public inserts" (INSERT with CHECK true)

JAVASCRIPT КОД ДЛЯ ИНТЕГРАЦИИ:
------------------------------
const SUPABASE_URL = 'https://fsovbwvbhwcdqebbxwdn.supabase.co';
const SUPABASE_ANON_KEY = 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6ImZzb3Zid3ZiaHdjZHFlYmJ4d2RuIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NjQwODc3ODgsImV4cCI6MjA3OTY2Mzc4OH0.QH3E4GVvcDzKdZAbLCw2MqcOqHmPVONZ_SwdECmdY08';
const supabase = window.supabase.createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

ПРИМЕР ИСПОЛЬЗОВАНИЯ:
---------------------
// Отправка данных формы
async function submitForm(name, email, message) {
  const { data, error } = await supabase
    .from('contacts')
    .insert([
      { name, email, message }
    ]);
  
  if (error) {
    console.error('Error:', error);
  } else {
    console.log('Success:', data);
  }
}

ССЫЛКИ:
-------
Dashboard: https://supabase.com/dashboard/project/fsovbwvbhwcdqebbxwdn
API Settings: https://supabase.com/dashboard/project/fsovbwvbhwcdqebbxwdn/settings/api


ВОТ- GOOGLE CLOUD СТРАНИЦЫ ДЕПЛОЯ- https://console.cloud.google.com/storage/browser/prytkov-portfolio-2025-v1;tab=objects?project=gen-lang-client-0468820155&prefix=&forceOnObjectsSortingFiltering=false