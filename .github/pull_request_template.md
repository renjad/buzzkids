## 📋 Description

<!-- Provide a brief description of what this PR does -->

## 🎫 Related Task

<!-- Link to Jira task -->

Closes BUZZ-XXX

<!-- Example: Closes BUZZ-25 -->

## 🔧 Type of Change

<!-- Mark with 'x' -->

- [ ] New feature (non-breaking change which adds functionality)
- [ ] Bug fix (non-breaking change which fixes an issue)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] Documentation update
- [ ] Code refactoring
- [ ] Performance improvement

## ✅ Testing Checklist

<!-- All items must be checked before requesting review -->

### Tests Written

- [ ] Feature tests added/updated
- [ ] Unit tests added/updated (if applicable)
- [ ] All tests pass locally (`sail test`)
- [ ] No test failures or warnings

### Manual Testing

- [ ] Tested feature in browser
- [ ] Tested on mobile viewport (if UI change)
- [ ] No console errors
- [ ] No visual regressions

### Test Coverage

- [ ] Happy path tested
- [ ] Edge cases tested
- [ ] Error scenarios tested

## 🎨 Screenshots / Videos (if UI changes)

<!-- Add screenshots or GIFs showing the changes -->

**Before:**

<!-- Screenshot of before state -->

**After:**

<!-- Screenshot of after state -->

## 📝 Code Quality Checklist

<!-- All items must be checked -->

- [ ] Code follows PSR-12 coding standards
- [ ] Self-review completed
- [ ] Comments added for complex logic
- [ ] No commented-out code left behind
- [ ] No debug statements (dd, dump, console.log, var_dump)
- [ ] Variable and function names are descriptive
- [ ] No unnecessary code duplication

## 🗄️ Database Changes

<!-- If this PR includes database changes -->

- [ ] Migration files added
- [ ] Migration tested (up and down)
- [ ] Seeder updated (if applicable)
- [ ] No data loss on migration

**OR**

- [ ] No database changes in this PR

## 📦 Dependencies

<!-- List any new packages or dependencies added -->

- [ ] No new dependencies added

**OR**

New dependencies:

- Package name: version - reason for adding

## 🔒 Security Considerations

<!-- Any security implications? -->

- [ ] No security implications
- [ ] User input is validated
- [ ] Data is sanitized
- [ ] Authorization checks in place
- [ ] No sensitive data exposed

## ⚡ Performance Impact

<!-- Any performance considerations? -->

- [ ] No performance impact
- [ ] Queries are optimized
- [ ] N+1 queries avoided
- [ ] Appropriate indexes added

## 📚 Documentation

<!-- Documentation updates -->

- [ ] README updated (if needed)
- [ ] API documentation updated (if needed)
- [ ] Comments added for complex code
- [ ] No documentation needed

## 🚀 Deployment Notes

<!-- Anything special needed for deployment? -->

- [ ] No special deployment steps needed

**OR**

Special steps required:

1. Run migration: `php artisan migrate`
2. Clear cache: `php artisan cache:clear`
3. Other: ****\_\_\_****

## 👀 Review Focus Areas

<!-- Guide reviewers on what to focus on -->

Please pay special attention to:

-
-

## ⚠️ Breaking Changes

<!-- Any breaking changes? -->

- [ ] No breaking changes

**OR**

Breaking changes:

-

## 📌 Additional Notes

<!-- Any other information reviewers should know -->

---

## ✅ Final Checklist

<!-- ALL must be checked before requesting review -->

- [ ] I have performed a self-review of my code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings
- [ ] I have added tests that prove my fix is effective or that my feature works
- [ ] New and existing unit tests pass locally with my changes
- [ ] Any dependent changes have been merged and published

---

**⚠️ Reminder:** PRs without completed checklists will be sent back for completion.
