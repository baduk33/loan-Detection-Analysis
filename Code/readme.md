# For data cleaning
df.isnull().sum()

**Annual Income BY Gender**

```
plt.figure(figsize=(3,3))
sns.kdeplot(data = df, x = "Annual_Income", hue = "Gender", palette= "muted" )
plt.xlabel('Annual Income')
plt.ylabel('Density')
plt.title('Annual Income By Gender')
plt.legend(title='Gender', labels=['Male', 'Female'])
plt.show()
```

# Income Distribution By Gender
```
sns.violinplot(x='Education', y='Annual_Income', data=df, color="salmon", inner = "point", density_norm='count', width = 0.5, alpha=0.6)
plt.title('Income Distribution by Education')
plt.show()
```
**How Income, Loan Amount & Credit Score Are Distributed**
```
plt.figure(figsize=(9,5))
bins = 30

plt.hist(df['Annual_Income'], bins=bins, alpha=0.5, label='Annual Income', color='lightgreen', edgecolor='black', density=True)
plt.hist(df['Loan_Amount'], bins=bins, alpha=0.5, label='Loan Amount', color='salmon', edgecolor='black', density=True)
plt.hist(df['Credit_Score'], bins=bins, alpha=0.5, label='Credit Score', color='skyblue', edgecolor='black', density=True)

plt.title('How Income, Loan Amount & Credit Score Are Distributed')
plt.xlabel('Value')
plt.ylabel('Density')
plt.legend()
plt.grid(axis='y', linestyle='--', alpha=0.6)
plt.xlim(0, 12000)
plt.grid()
plt.tight_layout()
plt.show()
```
