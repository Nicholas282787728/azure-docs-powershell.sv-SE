---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADUser.md
ms.openlocfilehash: 2fe2162221672522596065ef615a8098bfc12a60
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923722"
---
# <span data-ttu-id="d31b0-101">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="d31b0-101">Update-AzADUser</span></span>

## <span data-ttu-id="d31b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d31b0-102">SYNOPSIS</span></span>
<span data-ttu-id="d31b0-103">Uppdaterar en befintlig Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="d31b0-103">Updates an existing active directory user.</span></span>

## <span data-ttu-id="d31b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d31b0-104">SYNTAX</span></span>

### <span data-ttu-id="d31b0-105">UPNOrObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d31b0-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d31b0-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d31b0-106">UPNParameterSet</span></span>
```
Update-AzADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d31b0-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d31b0-107">ObjectIdParameterSet</span></span>
```
Update-AzADUser -ObjectId <Guid> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d31b0-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d31b0-108">InputObjectParameterSet</span></span>
```
Update-AzADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d31b0-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d31b0-109">DESCRIPTION</span></span>
<span data-ttu-id="d31b0-110">Uppdaterar en befintlig Active Directory-användare (arbets-eller skol konto som också kallas organisations-ID).</span><span class="sxs-lookup"><span data-stu-id="d31b0-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="d31b0-111">Mer information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="d31b0-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="d31b0-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d31b0-112">EXAMPLES</span></span>

### <span data-ttu-id="d31b0-113">Exempel 1 – uppdatera visnings namnet för en användare med hjälp av objekt-ID</span><span class="sxs-lookup"><span data-stu-id="d31b0-113">Example 1 - Update the display name of a user using object id</span></span>

```
PS C:\> Update-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="d31b0-114">Uppdaterar visnings namnet för användaren med objekt-ID ' 155a5c10-93a9-4941-a0df-96d83ab5ab24 ' som ska vara ' MyNewDisplayName '.</span><span class="sxs-lookup"><span data-stu-id="d31b0-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="d31b0-115">Exempel 2 – uppdatera visnings namnet för en användare med UPN-namn</span><span class="sxs-lookup"><span data-stu-id="d31b0-115">Example 2 - Update the display name of a user using user principal name</span></span>

```
PS C:\> Update-AzADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="d31b0-116">Uppdaterar visnings namnet för användaren med huvud namnet " foo@domain.com ' MyNewDisplayName '.</span><span class="sxs-lookup"><span data-stu-id="d31b0-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="d31b0-117">Exempel 3 – uppdatera visnings namnet för en användare med hjälp av rör</span><span class="sxs-lookup"><span data-stu-id="d31b0-117">Example 3 - Update the display name of a user using piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="d31b0-118">Hämtar användaren med objekt-ID ' 155a5c10-93a9-4941-a0df-96d83ab5ab24 ' och pipes till Update-AzADUser cmdlet för att uppdatera visnings namnet för den användaren till "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="d31b0-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="d31b0-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d31b0-119">PARAMETERS</span></span>

### <span data-ttu-id="d31b0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d31b0-120">-DefaultProfile</span></span>
<span data-ttu-id="d31b0-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d31b0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d31b0-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d31b0-122">-DisplayName</span></span>
<span data-ttu-id="d31b0-123">Nytt visnings namn för användaren.</span><span class="sxs-lookup"><span data-stu-id="d31b0-123">New display name for the user.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d31b0-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="d31b0-124">-EnableAccount</span></span>
<span data-ttu-id="d31b0-125">sant för att aktivera kontot annars FALSE.</span><span class="sxs-lookup"><span data-stu-id="d31b0-125">true for enabling the account; otherwise, false.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d31b0-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="d31b0-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="d31b0-127">Det måste anges om användaren bör ändra lösen ordet vid nästa lyckade inloggning.</span><span class="sxs-lookup"><span data-stu-id="d31b0-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="d31b0-128">Endast giltigt om lösen ordet uppdateras annars kommer det att ignoreras.</span><span class="sxs-lookup"><span data-stu-id="d31b0-128">Only valid if password is updated otherwise it will be ignored.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d31b0-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d31b0-129">-InputObject</span></span>
<span data-ttu-id="d31b0-130">Det objekt som representerar den användare som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="d31b0-130">The object representing the user to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d31b0-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d31b0-131">-ObjectId</span></span>
<span data-ttu-id="d31b0-132">Objekt-ID för den användare som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="d31b0-132">The object id of the user to be updated.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d31b0-133">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="d31b0-133">-Password</span></span>
<span data-ttu-id="d31b0-134">Nytt lösen ord för användaren.</span><span class="sxs-lookup"><span data-stu-id="d31b0-134">New password for the user.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d31b0-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="d31b0-135">-UPNOrObjectId</span></span>
<span data-ttu-id="d31b0-136">Användarens huvud namn eller objekt-ID för den användare som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="d31b0-136">The user principal name or object id of the user to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d31b0-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d31b0-137">-UserPrincipalName</span></span>
<span data-ttu-id="d31b0-138">Användarens huvud namn för den användare som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="d31b0-138">The user principal name of the user to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d31b0-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d31b0-139">-Confirm</span></span>
<span data-ttu-id="d31b0-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d31b0-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d31b0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d31b0-141">-WhatIf</span></span>
<span data-ttu-id="d31b0-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d31b0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d31b0-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d31b0-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d31b0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d31b0-144">CommonParameters</span></span>
<span data-ttu-id="d31b0-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d31b0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d31b0-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d31b0-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d31b0-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d31b0-147">INPUTS</span></span>

### <span data-ttu-id="d31b0-148">System. String</span><span class="sxs-lookup"><span data-stu-id="d31b0-148">System.String</span></span>

### <span data-ttu-id="d31b0-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d31b0-149">System.Guid</span></span>

### <span data-ttu-id="d31b0-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="d31b0-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="d31b0-151">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d31b0-151">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="d31b0-152">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d31b0-152">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d31b0-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="d31b0-153">System.Security.SecureString</span></span>

## <span data-ttu-id="d31b0-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d31b0-154">OUTPUTS</span></span>

### <span data-ttu-id="d31b0-155">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="d31b0-155">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="d31b0-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d31b0-156">NOTES</span></span>

## <span data-ttu-id="d31b0-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d31b0-157">RELATED LINKS</span></span>
