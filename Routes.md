Tips:
- don't name 2 params in the same route the same thing
- check out shallow nesting - try to nest only when you *need* the parent information to complete the route purpose
- how do we add a student to a class? there doesn't seem to be a route for this
- similarly, can we remove a student from a class?
- Does each student always have to be created with a class and/or always have to have at least one class? 

```
           Prefix Verb   URI Pattern                            Controller#Action       Purpose
             root GET    /                                      index#show              home page
            about GET    /about .                               about#index             about page
         students GET    classes/:id/students(.:format)         students#index          show all students in a class
      new_student GET    /students/new(.:format)                students#new            new student form (not class-dependent)
                  POST   /students(.:format)                    students#create         add a student to db
          student GET    /classes/:id/students/:id(.:format)    students#show           view one student in one class ?? (might not need to be nested)
     edit_student GET    /students/:id/edit(.:format)           students#edit           edit form for one student, not class-dependent
                  PATCH  /students/:id(.:format)                students#update         update student
         teachers GET    /classes/:id/teachers(.:format)        teachers#index          waiting to examine teacher routes
      new_teacher GET    /teachers/new(.:format)                teachers#new            ^
                  POST   /teachers(.:format)                    teachers#create         ^
          teacher GET    /teachers/:id(.:format)                teachers#show           ^
     edit_teacher GET    /teachers/:id/edit(.:format)           teachers#edit           ^
                  PATCH  /teachers/:id(.:format)                teachers#update         ^        
            login GET    /login(.:format)                       sessions#new            login form
         sessions POST   /sessions(.:format)                    sessions#create         actually log user in (login form submits here)
           logout GET    /logout(.:format)                      sessions#destroy        logout 'button/link' - actually log user out
            class GET    /classes/:id(.:format)                 classes#show            details for one class
      assignments GET    /classes/:id/assignments/(.:format)    assignment#index        all assignments for one class
   new_assignment GET    /classes/:id/assignments/new(.:format) assignments#new         new assignment form for one class
create_assignment POST   /classes/:id/assignments(.:format)     assignments#create      create ssignmetn for one class
  edit_assignment GET    /classes/:id/assignments(.:format)     assignments#edit        edit form for which assignment??? (NEEDS ID) for one class
       assignment GET    /assignments/:id(.:format) assignments#show
                  PATCH  /classes/:id/assignments/:id           assignments#update      acutally update class (match this uri ofr edit form)    
                  DELETE /assignments/:id                       assignments#destroy     rm assignment
   new_submission GET    /assignments/:id/submission/new        submission#new          new submission form
create_submission POST   /assignments/:id/submission/           submission#create       acutally create submission
  edit_submission GET    /assignments/:id/submission/:id        submission#edit         edit specific submission for specific assignment (uri params cant' both be called id)
       submission GET    /submissions/:id                       submission#show         good use of non-nested
                  PATCH  /submissions/:id                       submission#show         shouldn't go to #show
                  DELETE /submissions/:id .                     submission#destroy      

##Feedback routes for first version of site
   new_assignment_feedback GET    /assignments/:assignment_id/feedbacks/new    feedback#new        feedback form
create_assignment_feedback POST   /assignments/:assignment_id/feedbacks        feedback#create     actually create feedback for as.
  edit_assignment_feedback GET    /assignments/:assignment_id/feedbacks/:id    feedback#edit       edit form, specific feedback (doesn't need to be nested)
       assignment_feedback GET    /feedbacks/:id                               feedback#show       show one fb
                           PATCH  /assignments/:assignment_id/feedbacks/:id    feedbacks#update    actually edit (doesnt need to be nested?) 
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
