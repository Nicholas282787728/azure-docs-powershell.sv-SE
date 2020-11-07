---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: 091f54b69cd713d93def4c727181f9c8e7d5b0d6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923850"
---
# <span data-ttu-id="72cae-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="72cae-101">Remove-AzADUser</span></span>

## <span data-ttu-id="72cae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72cae-102">SYNOPSIS</span></span>
<span data-ttu-id="72cae-103">Tar bort en Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="72cae-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="72cae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72cae-104">SYNTAX</span></span>

### <span data-ttu-id="72cae-105">UPNOrObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="72cae-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72cae-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="72cae-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72cae-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="72cae-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72cae-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="72cae-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72cae-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="72cae-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72cae-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72cae-110">DESCRIPTION</span></span>
<span data-ttu-id="72cae-111">Tar bort en Active Directory-användare (arbets-eller skol konto som också kallas organisations-ID).</span><span class="sxs-lookup"><span data-stu-id="72cae-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="72cae-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72cae-112">EXAMPLES</span></span>

### <span data-ttu-id="72cae-113">Exempel 1 – ta bort en användare via huvud namnet för användare</span><span class="sxs-lookup"><span data-stu-id="72cae-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="72cae-114">Tar bort användaren med UPN-namnet " foo@domain.com " från innehavaren.</span><span class="sxs-lookup"><span data-stu-id="72cae-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="72cae-115">Exempel 2 – ta bort en användare utifrån objekt-ID</span><span class="sxs-lookup"><span data-stu-id="72cae-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="72cae-116">Tar bort användaren med objekt-ID ' 7a9582cf-88c4-4319-842b-7a5d60967a69 ' från innehavaren.</span><span class="sxs-lookup"><span data-stu-id="72cae-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="72cae-117">Exempel 3 – ta bort en användare genom rör</span><span class="sxs-lookup"><span data-stu-id="72cae-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="72cae-118">Hämtar användaren med objekt-ID ' 7a9582cf-88c4-4319-842b-7a5d60967a69 ' och pipes till Remove-AzADUser cmdlet för att ta bort användaren från klient organisationen.</span><span class="sxs-lookup"><span data-stu-id="72cae-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="72cae-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72cae-119">PARAMETERS</span></span>

### <span data-ttu-id="72cae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72cae-120">-DefaultProfile</span></span>
<span data-ttu-id="72cae-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="72cae-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72cae-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="72cae-122">-DisplayName</span></span>
<span data-ttu-id="72cae-123">Visnings namnet på den användare som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="72cae-123">The display name of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72cae-124">-Force</span><span class="sxs-lookup"><span data-stu-id="72cae-124">-Force</span></span>
<span data-ttu-id="72cae-125">Om det anges ber vi dig bekräfta att du vill ta bort användaren.</span><span class="sxs-lookup"><span data-stu-id="72cae-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="72cae-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72cae-126">-InputObject</span></span>
<span data-ttu-id="72cae-127">Användarobjektet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="72cae-127">The user object to be deleted.</span></span>

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

### <span data-ttu-id="72cae-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="72cae-128">-ObjectId</span></span>
<span data-ttu-id="72cae-129">Objekt-ID för den användare som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="72cae-129">The object id of the user to be deleted.</span></span>

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

### <span data-ttu-id="72cae-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72cae-130">-PassThru</span></span>
<span data-ttu-id="72cae-131">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="72cae-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="72cae-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="72cae-132">-UPNOrObjectId</span></span>
<span data-ttu-id="72cae-133">Användarens huvud namn eller objectId för den användare som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="72cae-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="72cae-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="72cae-134">-UserPrincipalName</span></span>
<span data-ttu-id="72cae-135">Användarens huvud namn för den användare som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="72cae-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="72cae-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="72cae-136">-Confirm</span></span>
<span data-ttu-id="72cae-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="72cae-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72cae-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72cae-138">-WhatIf</span></span>
<span data-ttu-id="72cae-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="72cae-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72cae-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="72cae-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72cae-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72cae-141">CommonParameters</span></span>
<span data-ttu-id="72cae-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72cae-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72cae-143">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72cae-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72cae-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72cae-144">INPUTS</span></span>

### <span data-ttu-id="72cae-145">System. String</span><span class="sxs-lookup"><span data-stu-id="72cae-145">System.String</span></span>

### <span data-ttu-id="72cae-146">System. GUID</span><span class="sxs-lookup"><span data-stu-id="72cae-146">System.Guid</span></span>

### <span data-ttu-id="72cae-147">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="72cae-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="72cae-148">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="72cae-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="72cae-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72cae-149">OUTPUTS</span></span>

### <span data-ttu-id="72cae-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72cae-150">System.Boolean</span></span>

## <span data-ttu-id="72cae-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72cae-151">NOTES</span></span>

## <span data-ttu-id="72cae-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72cae-152">RELATED LINKS</span></span>

[<span data-ttu-id="72cae-153">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="72cae-153">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="72cae-154">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="72cae-154">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="72cae-155">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="72cae-155">Set-AzADUser</span></span>](./Set-AzADUser.md)

