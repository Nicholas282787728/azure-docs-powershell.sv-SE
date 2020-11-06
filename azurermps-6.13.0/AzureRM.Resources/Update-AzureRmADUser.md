---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmADUser.md
ms.openlocfilehash: a07d9119d5e83c92d96ab22e98125459945f786b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576094"
---
# <span data-ttu-id="a1b75-101">Update-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a1b75-101">Update-AzureRmADUser</span></span>

## <span data-ttu-id="a1b75-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1b75-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b75-103">Uppdaterar en befintlig Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="a1b75-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1b75-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1b75-104">SYNTAX</span></span>

### <span data-ttu-id="a1b75-105">UPNOrObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a1b75-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1b75-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1b75-106">UPNParameterSet</span></span>
```
Update-AzureRmADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1b75-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1b75-107">ObjectIdParameterSet</span></span>
```
Update-AzureRmADUser -ObjectId <Guid> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1b75-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1b75-108">InputObjectParameterSet</span></span>
```
Update-AzureRmADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1b75-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1b75-109">DESCRIPTION</span></span>
<span data-ttu-id="a1b75-110">Uppdaterar en befintlig Active Directory-användare (arbets-eller skol konto som också kallas organisations-ID).</span><span class="sxs-lookup"><span data-stu-id="a1b75-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="a1b75-111">Mer information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="a1b75-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="a1b75-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1b75-112">EXAMPLES</span></span>

### <span data-ttu-id="a1b75-113">Exempel 1 – uppdatera visnings namnet för en användare med hjälp av objekt-ID</span><span class="sxs-lookup"><span data-stu-id="a1b75-113">Example 1 - Update the display name of a user using object id</span></span>

```
PS C:\> Update-AzureRmADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="a1b75-114">Uppdaterar visnings namnet för användaren med objekt-ID ' 155a5c10-93a9-4941-a0df-96d83ab5ab24 ' som ska vara ' MyNewDisplayName '.</span><span class="sxs-lookup"><span data-stu-id="a1b75-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="a1b75-115">Exempel 2 – uppdatera visnings namnet för en användare med UPN-namn</span><span class="sxs-lookup"><span data-stu-id="a1b75-115">Example 2 - Update the display name of a user using user principal name</span></span>

```
PS C:\> Update-AzureRmADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="a1b75-116">Uppdaterar visnings namnet för användaren med huvud namnet " foo@domain.com ' MyNewDisplayName '.</span><span class="sxs-lookup"><span data-stu-id="a1b75-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="a1b75-117">Exempel 3 – uppdatera visnings namnet för en användare med hjälp av rör</span><span class="sxs-lookup"><span data-stu-id="a1b75-117">Example 3 - Update the display name of a user using piping</span></span>

```
PS C:\> Get-AzureRmADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzureRmADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="a1b75-118">Hämtar användaren med objekt-ID ' 155a5c10-93a9-4941-a0df-96d83ab5ab24 ' och pipes till Update-AzureRmADUser cmdlet för att uppdatera visnings namnet för den användaren till "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="a1b75-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzureRmADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="a1b75-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1b75-119">PARAMETERS</span></span>

### <span data-ttu-id="a1b75-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b75-120">-DefaultProfile</span></span>
<span data-ttu-id="a1b75-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b75-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b75-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a1b75-122">-DisplayName</span></span>
<span data-ttu-id="a1b75-123">Nytt visnings namn för användaren.</span><span class="sxs-lookup"><span data-stu-id="a1b75-123">New display name for the user.</span></span>

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

### <span data-ttu-id="a1b75-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="a1b75-124">-EnableAccount</span></span>
<span data-ttu-id="a1b75-125">sant för att aktivera kontot annars FALSE.</span><span class="sxs-lookup"><span data-stu-id="a1b75-125">true for enabling the account; otherwise, false.</span></span>

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

### <span data-ttu-id="a1b75-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="a1b75-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="a1b75-127">Det måste anges om användaren bör ändra lösen ordet vid nästa lyckade inloggning.</span><span class="sxs-lookup"><span data-stu-id="a1b75-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="a1b75-128">Endast giltigt om lösen ordet uppdateras annars kommer det att ignoreras.</span><span class="sxs-lookup"><span data-stu-id="a1b75-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="a1b75-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1b75-129">-InputObject</span></span>
<span data-ttu-id="a1b75-130">Det objekt som representerar den användare som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="a1b75-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="a1b75-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a1b75-131">-ObjectId</span></span>
<span data-ttu-id="a1b75-132">Objekt-ID för den användare som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="a1b75-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="a1b75-133">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="a1b75-133">-Password</span></span>
<span data-ttu-id="a1b75-134">Nytt lösen ord för användaren.</span><span class="sxs-lookup"><span data-stu-id="a1b75-134">New password for the user.</span></span>

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

### <span data-ttu-id="a1b75-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="a1b75-135">-UPNOrObjectId</span></span>
<span data-ttu-id="a1b75-136">Användarens huvud namn eller objekt-ID för den användare som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="a1b75-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="a1b75-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a1b75-137">-UserPrincipalName</span></span>
<span data-ttu-id="a1b75-138">Användarens huvud namn för den användare som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="a1b75-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="a1b75-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a1b75-139">-Confirm</span></span>
<span data-ttu-id="a1b75-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a1b75-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1b75-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1b75-141">-WhatIf</span></span>
<span data-ttu-id="a1b75-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a1b75-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1b75-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a1b75-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1b75-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b75-144">CommonParameters</span></span>
<span data-ttu-id="a1b75-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1b75-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b75-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1b75-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b75-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1b75-147">INPUTS</span></span>

### <span data-ttu-id="a1b75-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a1b75-148">System.String</span></span>

### <span data-ttu-id="a1b75-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a1b75-149">System.Guid</span></span>

### <span data-ttu-id="a1b75-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="a1b75-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="a1b75-151">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a1b75-151">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a1b75-152">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a1b75-152">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a1b75-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="a1b75-153">System.Security.SecureString</span></span>

## <span data-ttu-id="a1b75-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1b75-154">OUTPUTS</span></span>

### <span data-ttu-id="a1b75-155">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="a1b75-155">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="a1b75-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1b75-156">NOTES</span></span>

## <span data-ttu-id="a1b75-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1b75-157">RELATED LINKS</span></span>
