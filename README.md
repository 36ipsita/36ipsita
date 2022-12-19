def read_test_scores():
    print("ENTER STUDENT ID: ")
    id = int(input())

    print("ENTER EXAM SCORE: ")
    exam = int(input())

    print("ENTER ALL TEST SCORES: ")
    score1 = int(input())
    score2 = int(input())
    score3 = int(input())
    score4 = int(input())
    score5 = int(input())
    score6 = int(input())

    sum = (score1 + score2 + score3 + score4 + score5 + score6)

    tavge = sum / 7.0
    return tavge, id, exam


def compute_final_score(tavge, exam):
    final_score = 0.4 * tavge + 0.6 * exam
    return final_score


def get_letter_grade(final_score):
    if 90 <= final_score <= 100:
        grade = 'A'
    elif 80 <= final_score <= 89:
        grade = 'B'
    elif 70 <= final_score <= 79:
        grade = 'C'
    elif 60 <= final_score <= 69:
        grade = 'D'
    else:
        grade = 'F'
    return grade


def print_comment(grade):

    if grade == 'A':
        print("COMMENT:            Very Good")
    elif grade == 'B':
        print("COMMENT:            Good")
    elif grade == 'C':
        print("COMMENT:            Satisfactory")
    elif grade == 'D':
        print("COMMENT:            Need Improvement")
    elif grade == 'F':
        print("COMMENT:            Poor")


tavge, id, exam = read_test_scores()
print ("TEST AVERAGE IS:    " + str(tavge))

my_variable = compute_final_score(tavge, exam)
print("FINAL SCORE IS:     " + str(my_variable))
grade = get_letter_grade(my_variable)
print("LETTER GRADE IS:     " + str(grade))
print_comment(grade)
