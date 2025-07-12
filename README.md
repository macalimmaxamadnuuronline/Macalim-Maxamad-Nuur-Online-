policyname  |  cmd   |                    qual                    |                 with_check
--------------+--------+--------------------------------------------+--------------------------------------------
 create todos | INSERT |                                            | ( SELECT (auth.user_id() = todos.user_id))
 update todos | UPDATE | ( SELECT (auth.user_id() = todos.user_id)) |
 delete todos | DELETE | ( SELECT (auth.user_id() = todos.user_id)) |
 view todos   | SELECT | ( SELECT (auth.user_id() = todos.user_id)) |
(4 rows)
