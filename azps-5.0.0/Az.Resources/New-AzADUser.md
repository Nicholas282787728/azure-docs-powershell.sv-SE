---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
ms.openlocfilehash: c7863e62330dc26d9733d21eb8e4d11753e06d1c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322836"
---
# <span data-ttu-id="ee1c0-101">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ee1c0-101">New-AzADUser</span></span>

## <span data-ttu-id="ee1c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee1c0-102">SYNOPSIS</span></span>
<span data-ttu-id="ee1c0-103">Skapar en ny Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="ee1c0-103">Creates a new active directory user.</span></span>

## <span data-ttu-id="ee1c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee1c0-104">SYNTAX</span></span>

```
New-AzADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString> [-ImmutableId <String>]
 -MailNickname <String> [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee1c0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee1c0-105">DESCRIPTION</span></span>
<span data-ttu-id="ee1c0-106">Skapar en ny Active Directory-användare (arbets-eller skol konto som också kallas organisations-ID).</span><span class="sxs-lookup"><span data-stu-id="ee1c0-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="ee1c0-107">Mer information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="ee1c0-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="ee1c0-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee1c0-108">EXAMPLES</span></span>

### <span data-ttu-id="ee1c0-109">Exempel 1: skapa en ny AD-användare</span><span class="sxs-lookup"><span data-stu-id="ee1c0-109">Example 1: Create a new AD user</span></span>
```powershell
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="ee1c0-110">Skapar en ny AD-användare med namnet "visnings namn" och användarens huvud namn " myemail@domain.com " i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="ee1c0-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="ee1c0-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee1c0-111">PARAMETERS</span></span>

### <span data-ttu-id="ee1c0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee1c0-112">-DefaultProfile</span></span>
<span data-ttu-id="ee1c0-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ee1c0-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee1c0-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ee1c0-114">-DisplayName</span></span>
<span data-ttu-id="ee1c0-115">Det namn som ska visas i adress boken för användaren.</span><span class="sxs-lookup"><span data-stu-id="ee1c0-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="ee1c0-116">exempel "Alex Wu".</span><span class="sxs-lookup"><span data-stu-id="ee1c0-116">example 'Alex Wu'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1c0-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="ee1c0-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="ee1c0-118">Det måste anges om användaren måste ändra lösen ordet vid nästa lyckade inloggning (sant).</span><span class="sxs-lookup"><span data-stu-id="ee1c0-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="ee1c0-119">Standard beteende är (falskt) för att inte ändra lösen ordet vid nästa lyckade inloggning.</span><span class="sxs-lookup"><span data-stu-id="ee1c0-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1c0-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="ee1c0-120">-ImmutableId</span></span>
<span data-ttu-id="ee1c0-121">Den måste anges bara om du använder en federerad domän som användarens huvud namn (UPN)-egenskap.</span><span class="sxs-lookup"><span data-stu-id="ee1c0-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1c0-122">-Smek namn</span><span class="sxs-lookup"><span data-stu-id="ee1c0-122">-MailNickname</span></span>
<span data-ttu-id="ee1c0-123">Användarens e-postalias.</span><span class="sxs-lookup"><span data-stu-id="ee1c0-123">The mail alias for the user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1c0-124">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="ee1c0-124">-Password</span></span>
<span data-ttu-id="ee1c0-125">Lösen ord för användaren.</span><span class="sxs-lookup"><span data-stu-id="ee1c0-125">Password for the user.</span></span>
<span data-ttu-id="ee1c0-126">Den måste uppfylla innehavarens komplexitets krav.</span><span class="sxs-lookup"><span data-stu-id="ee1c0-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="ee1c0-127">Vi rekommenderar att du anger ett starkt lösen ord.</span><span class="sxs-lookup"><span data-stu-id="ee1c0-127">It is recommended to set a strong password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1c0-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ee1c0-128">-UserPrincipalName</span></span>
<span data-ttu-id="ee1c0-129">Användarens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="ee1c0-129">The user principal name.</span></span>
<span data-ttu-id="ee1c0-130">Exempel-" someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="ee1c0-130">Example-'someuser@contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1c0-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ee1c0-131">-Confirm</span></span>
<span data-ttu-id="ee1c0-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ee1c0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee1c0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee1c0-133">-WhatIf</span></span>
<span data-ttu-id="ee1c0-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ee1c0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee1c0-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ee1c0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee1c0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee1c0-136">CommonParameters</span></span>
<span data-ttu-id="ee1c0-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee1c0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee1c0-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee1c0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee1c0-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee1c0-139">INPUTS</span></span>

### <span data-ttu-id="ee1c0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ee1c0-140">System.String</span></span>

### <span data-ttu-id="ee1c0-141">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="ee1c0-141">System.Security.SecureString</span></span>

### <span data-ttu-id="ee1c0-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ee1c0-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ee1c0-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee1c0-143">OUTPUTS</span></span>

### <span data-ttu-id="ee1c0-144">Microsoft. Azure. commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="ee1c0-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="ee1c0-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee1c0-145">NOTES</span></span>

## <span data-ttu-id="ee1c0-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee1c0-146">RELATED LINKS</span></span>

[<span data-ttu-id="ee1c0-147">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ee1c0-147">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="ee1c0-148">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ee1c0-148">Update-AzADUser</span></span>](./Update-AzADUser.md)

[<span data-ttu-id="ee1c0-149">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ee1c0-149">Remove-AzADUser</span></span>](./Remove-AzADUser.md)