```
           Prefix Verb   URI Pattern                     Controller#Action
             root GET    /                                      index#show
            about GET    /about .                               about#index
         students GET    classes/:id/students(.:format)         students#index
      new_student GET    /students/new(.:format)                students#new
                  POST   /students(.:format)                    students#create
          student GET    /classes/:id/students/:id(.:format)    students#show
     edit_student GET    /students/:id/edit(.:format)           students#edit
                  PATCH  /students/:id(.:format)                students#update
         teachers GET    /classes/:id/teachers(.:format)        teachers#index
      new_teacher GET    /teachers/new(.:format)                teachers#new
                  POST   /teachers(.:format)                    teachers#create
          teacher GET    /teachers/:id(.:format)                teachers#show
     edit_teacher GET    /teachers/:id/edit(.:format)           teachers#edit
                  PATCH  /teachers/:id(.:format)                teachers#update                  
            login GET    /login(.:format)                       sessions#new
         sessions POST   /sessions(.:format)                    sessions#create
           logout GET    /logout(.:format)                      sessions#destroy
            class GET    /classes/:id(.:format)                 classes#show      
      assignments GET    /classes/:id/assignments/(.:format)    assignment#index    
   new_assignment GET    /classes/:id/assignments/new(.:format) assignments#new
create_assignment POST   /classes/:id/assignments(.:format)     assignments#create
  edit_assignment GET    /classes/:id/assignments(.:format)     assignments#edit
       assignment GET    /assignments/:id(.:format) assignments#show
                  PATCH  /classes/:id/assignments/:id           assignments#update
                  DELETE /assignments/:id                       assignments#destroy
   new_submission GET    /assignments/:id/submission/new        submission#new
create_submission POST   /assignments/:id/submission/           submission#create
  edit_submission GET    /assignments/:id/submission/:id        submission#edit
       submission GET    /submissions/:id                       submission#show
                  PATCH  /submissions/:id                       submission#show
                  DELETE /submissions/:id .                     submission#destroy

##Feedback routes for first version of site
   new_assignment_feedback GET    /assignments/:assignment_id/feedbacks/new    feedback#new
create_assignment_feedback POST   /assignments/:assignment_id/feedbacks        feedback#create
  edit_assignment_feedback GET    /assignments/:assignment_id/feedbacks/:id    feedback#edit
       assignment_feedback GET    /feedbacks/:id                               feedback#show
                           PATCH  /assignments/:assignment_id/feedbacks/:id    feedbacks#update
                           DELETE /assignments/:assignment_id/feedbacks/:id    feedbacks#destroy
                           
##Feedback routes to be added later
   new_teacher_feedback GET    /teachers/:teacher_id/feedbacks/new    feedback#new
create_teacher_feedback POST   /teachers/:teacher_id/feedbacks        feedback#create
  edit_teacher_feedback GET    /teachers/:teacher_id/feedbacks/:id    feedback#edit
       teacher_feedback GET    /feedbacks/:id                         feedback#show
                        PATCH  /teachers/:teacher_id/feedbacks/:id    feedbacks#update
                        DELETE /teachers/:teacher_id/feedbacks/:id    feedbacks#destroy
   new_student_feedback GET    /students/:student_id/feedbacks/new    feedback#new
create_student_feedback POST   /students/:student_id/feedbacks        feedback#create
  edit_student_feedback GET    /students/:student_id/feedbacks/:id    feedback#edit
       student_feedback GET    /feedbacks/:id                         feedback#show
                        PATCH  /students/:student_id/feedbacks/:id    feedbacks#update
                        DELETE /students/:student_id/feedbacks/:id    feedbacks#destroy
```
