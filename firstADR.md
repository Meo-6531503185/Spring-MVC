
# Title: Selecting Django as the Web Framework

# Context:
We choose Spring MVC because it offers building web applications with clear separation of concerns,
integrating with other Spring features and developing complex applications with a focus on maintainability.

# Decision:
After careful deliberation, we have decided to adopt Django as the web framework for our project.

# Rationale: Why do we choose this solution?
We choose Spring MVC for my web application because it offers a mature and well-supported framework with flexible configuration options and a clear separation of concerns through the MVC pattern. This makes our application maintainable, scalable, and secure, while also providing access to a wealth of resources and community support.

# Consequences
# Pros – What becomes easier?
It enables rapid and parallel development.
Development of the application becomes fast.
Easy for multiple developers to work together.
Easier to Update the application.
It is Easier to Debug because we have multiple levels in the application.
# Cons – What becomes more difficult?
Spring MVC has high complexity to develop the applications using this pattern.


# Sample Code:

from django.shortcuts import render
from .models import Product

def product_list(request):
    products = Product.objects.all()
    return render(request, 'products/product_list.html', {'products': products}) 

