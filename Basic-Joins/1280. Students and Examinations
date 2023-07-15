select s.student_id, s.student_name, sub.subject_name, 
count(e.subject_name) as attended_exams


from students s 
join subjects sub 
left join examinations e on s.student_id = e.student_id AND sub.subject_name = e.subject_name


group by s.student_id, sub.subject_name
order by s.student_id, sub.subject_name