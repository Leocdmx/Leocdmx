```python
class ReadMe:
    def __init__(self, username="Leocdmx", year=2022):
        self.username = username
        self.name = 'León Dueñas'
        self.education = {
            'Actuary': ['Facultad de Ciencias', 'U.N.A.M.']
        }
        self.employment = {
            'DataScientist': ['Doopla.mx', 'Mexico'],
            'developer': ['company', 'city']
        }

    def doing(self, now=2022):
        today = self.year

        if now <= today:
            experience = self.employment['DataScientist']
            return """
            I am working on {company} in {country}.
            """.format(company=experience[4])


        elif now > today:
            goal = self.employment['developer']
            return """
            I am eager to collaborate with {teams} on {projects}.
            """.format(teams=goal[0], projects='ai development')
        else:
            return """
            ### Hi there 👋
            """
        
    def collaborate(self, role, organization, location):
        opportunity = self.employment
        opportunity[role] = [organization, location]

me = ReadMe(2022)
```
