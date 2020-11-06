---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
ms.openlocfilehash: 80a35ac1a1087d9e74cb47c3297af3ded491e701
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576422"
---
# <span data-ttu-id="38b93-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="38b93-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="38b93-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38b93-102">SYNOPSIS</span></span>
<span data-ttu-id="38b93-103">Skapar en ny Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="38b93-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38b93-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38b93-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString>
 [-ImmutableId <String>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38b93-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38b93-105">DESCRIPTION</span></span>
<span data-ttu-id="38b93-106">Skapar en ny Active Directory-användare (arbets-eller skol konto som också kallas organisations-ID).</span><span class="sxs-lookup"><span data-stu-id="38b93-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="38b93-107">Mer information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="38b93-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="38b93-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38b93-108">EXAMPLES</span></span>

### <span data-ttu-id="38b93-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="38b93-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="38b93-110">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="38b93-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="38b93-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38b93-111">PARAMETERS</span></span>

### <span data-ttu-id="38b93-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b93-112">-DefaultProfile</span></span>
<span data-ttu-id="38b93-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="38b93-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b93-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="38b93-114">-DisplayName</span></span>
<span data-ttu-id="38b93-115">Det namn som ska visas i adress boken för användaren.</span><span class="sxs-lookup"><span data-stu-id="38b93-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="38b93-116">exempel "Alex Wu".</span><span class="sxs-lookup"><span data-stu-id="38b93-116">example 'Alex Wu'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b93-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="38b93-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="38b93-118">Det måste anges om användaren måste ändra lösen ordet vid nästa lyckade inloggning (sant).</span><span class="sxs-lookup"><span data-stu-id="38b93-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="38b93-119">Standard beteende är (falskt) för att inte ändra lösen ordet vid nästa lyckade inloggning.</span><span class="sxs-lookup"><span data-stu-id="38b93-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b93-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="38b93-120">-ImmutableId</span></span>
<span data-ttu-id="38b93-121">Den måste anges bara om du använder en federerad domän som användarens huvud namn (UPN)-egenskap.</span><span class="sxs-lookup"><span data-stu-id="38b93-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b93-122">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="38b93-122">-Password</span></span>
<span data-ttu-id="38b93-123">Lösen ord för användaren.</span><span class="sxs-lookup"><span data-stu-id="38b93-123">Password for the user.</span></span>
<span data-ttu-id="38b93-124">Den måste uppfylla innehavarens komplexitets krav.</span><span class="sxs-lookup"><span data-stu-id="38b93-124">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="38b93-125">Vi rekommenderar att du anger ett starkt lösen ord.</span><span class="sxs-lookup"><span data-stu-id="38b93-125">It is recommended to set a strong password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b93-126">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="38b93-126">-UserPrincipalName</span></span>
<span data-ttu-id="38b93-127">Användarens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="38b93-127">The user principal name.</span></span>
<span data-ttu-id="38b93-128">Exempel-" someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="38b93-128">Example-'someuser@contoso.com'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b93-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="38b93-129">-Confirm</span></span>
<span data-ttu-id="38b93-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="38b93-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b93-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38b93-131">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b93-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b93-132">CommonParameters</span></span>
<span data-ttu-id="38b93-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38b93-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b93-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38b93-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b93-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38b93-135">INPUTS</span></span>

### <span data-ttu-id="38b93-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="38b93-136">None</span></span>
<span data-ttu-id="38b93-137">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="38b93-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="38b93-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38b93-138">OUTPUTS</span></span>

### <span data-ttu-id="38b93-139">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="38b93-139">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="38b93-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38b93-140">NOTES</span></span>

## <span data-ttu-id="38b93-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38b93-141">RELATED LINKS</span></span>

[<span data-ttu-id="38b93-142">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="38b93-142">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="38b93-143">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="38b93-143">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="38b93-144">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="38b93-144">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
