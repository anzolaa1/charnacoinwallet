**1. Clone wallet sources**

```
git clone https://github.com/charnasol/charnacoinwallet.git
```

**2. Modify `CryptoNoteWallet.cmake`**
 
```
set(CN_PROJECT_NAME "charnacoin")
set(CN_CURRENCY_DISPLAY_NAME "CharnaCoin")
set(CN_CURRENCY_TICKER "CHRC")
```

**3. Set symbolic link to coin sources at the same level as `src`. For example:**

```
ln -s ../cryptonote cryptonote
```

Alternative way is to create git submodule:

```
git submodule add https://github.com/charnasol/charnacoin.git charnacoin
```

Replace URL with git remote repository of your coin.

**4. Build**

```
mkdir build && cd build && cmake .. && make
```
