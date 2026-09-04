# KeySuite V4.23.01 Upgrade

Base: V4.23 Full Clean

Changes:
- Removed the forced MOS -> Motor special case from Role Brand / Series Assigned.
- Removed the forced MOS -> Motor special case from Customer Brand / Series pricing.
- Removed the MOS built-in Motor family from Product navigation.
- MOS now follows saved Brand / Series master mappings like other selling brands.
- A real MOTOR mapping can still expose Motor for MOS or another normal selling brand.
- No Supabase database migration or Edge Function deployment is required.
