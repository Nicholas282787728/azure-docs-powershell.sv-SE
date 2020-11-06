---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
ms.openlocfilehash: 27b52e6b3cf58f530e15b2ddd2ff3873087dfc2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575116"
---
# <span data-ttu-id="56fc4-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="56fc4-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="56fc4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="56fc4-103">Skapar en ny Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="56fc4-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56fc4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56fc4-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString>
 [-ImmutableId <String>] [-MailNickname <String>] [-ForceChangePasswordNextLogin]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56fc4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56fc4-105">DESCRIPTION</span></span>
<span data-ttu-id="56fc4-106">Skapar en ny Active Directory-användare (arbets-eller skol konto som också kallas organisations-ID).</span><span class="sxs-lookup"><span data-stu-id="56fc4-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="56fc4-107">Mer information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="56fc4-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="56fc4-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56fc4-108">EXAMPLES</span></span>

### <span data-ttu-id="56fc4-109">Exempel 1 – Skapa en ny AD-användare</span><span class="sxs-lookup"><span data-stu-id="56fc4-109">Example 1 - Create a new AD user</span></span>
```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="56fc4-110">Skapar en ny AD-användare med namnet "visnings namn" och användarens huvud namn " myemail@domain.com " i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="56fc4-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="56fc4-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56fc4-111">PARAMETERS</span></span>

### <span data-ttu-id="56fc4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56fc4-112">-DefaultProfile</span></span>
<span data-ttu-id="56fc4-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="56fc4-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56fc4-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="56fc4-114">-DisplayName</span></span>
<span data-ttu-id="56fc4-115">Det namn som ska visas i adress boken för användaren.</span><span class="sxs-lookup"><span data-stu-id="56fc4-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="56fc4-116">exempel "Alex Wu".</span><span class="sxs-lookup"><span data-stu-id="56fc4-116">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="56fc4-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="56fc4-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="56fc4-118">Det måste anges om användaren måste ändra lösen ordet vid nästa lyckade inloggning (sant).</span><span class="sxs-lookup"><span data-stu-id="56fc4-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="56fc4-119">Standard beteende är (falskt) för att inte ändra lösen ordet vid nästa lyckade inloggning.</span><span class="sxs-lookup"><span data-stu-id="56fc4-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="56fc4-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="56fc4-120">-ImmutableId</span></span>
<span data-ttu-id="56fc4-121">Den måste anges bara om du använder en federerad domän som användarens huvud namn (UPN)-egenskap.</span><span class="sxs-lookup"><span data-stu-id="56fc4-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="56fc4-122">-Smek namn</span><span class="sxs-lookup"><span data-stu-id="56fc4-122">-MailNickname</span></span>
<span data-ttu-id="56fc4-123">Användarens e-postalias.</span><span class="sxs-lookup"><span data-stu-id="56fc4-123">The mail alias for the user.</span></span>

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

### <span data-ttu-id="56fc4-124">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="56fc4-124">-Password</span></span>
<span data-ttu-id="56fc4-125">Lösen ord för användaren.</span><span class="sxs-lookup"><span data-stu-id="56fc4-125">Password for the user.</span></span>
<span data-ttu-id="56fc4-126">Den måste uppfylla innehavarens komplexitets krav.</span><span class="sxs-lookup"><span data-stu-id="56fc4-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="56fc4-127">Vi rekommenderar att du anger ett starkt lösen ord.</span><span class="sxs-lookup"><span data-stu-id="56fc4-127">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="56fc4-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="56fc4-128">-UserPrincipalName</span></span>
<span data-ttu-id="56fc4-129">Användarens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="56fc4-129">The user principal name.</span></span>
<span data-ttu-id="56fc4-130">Exempel-" someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="56fc4-130">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="56fc4-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="56fc4-131">-Confirm</span></span>
<span data-ttu-id="56fc4-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="56fc4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56fc4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56fc4-133">-WhatIf</span></span>
<span data-ttu-id="56fc4-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="56fc4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56fc4-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="56fc4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56fc4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56fc4-136">CommonParameters</span></span>
<span data-ttu-id="56fc4-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56fc4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56fc4-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56fc4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56fc4-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56fc4-139">INPUTS</span></span>

### <span data-ttu-id="56fc4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="56fc4-140">System.String</span></span>

### <span data-ttu-id="56fc4-141">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="56fc4-141">System.Security.SecureString</span></span>

### <span data-ttu-id="56fc4-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="56fc4-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="56fc4-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56fc4-143">OUTPUTS</span></span>

### <span data-ttu-id="56fc4-144">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="56fc4-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="56fc4-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56fc4-145">NOTES</span></span>

## <span data-ttu-id="56fc4-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56fc4-146">RELATED LINKS</span></span>

[<span data-ttu-id="56fc4-147">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="56fc4-147">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="56fc4-148">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="56fc4-148">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="56fc4-149">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="56fc4-149">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
