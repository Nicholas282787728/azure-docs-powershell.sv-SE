---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
ms.openlocfilehash: ec9c234a03180f20b1b0cf6a4f5004923f3eab51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585335"
---
# <span data-ttu-id="d51c9-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="d51c9-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="d51c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d51c9-102">SYNOPSIS</span></span>
<span data-ttu-id="d51c9-103">Skapar en ny Active Directory-användare.</span><span class="sxs-lookup"><span data-stu-id="d51c9-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d51c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d51c9-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <String> [-ImmutableId <String>]
 [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d51c9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d51c9-105">DESCRIPTION</span></span>
<span data-ttu-id="d51c9-106">Skapar en ny Active Directory-användare (arbets-eller skol konto som också kallas organisations-ID).</span><span class="sxs-lookup"><span data-stu-id="d51c9-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="d51c9-107">Mer information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="d51c9-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="d51c9-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d51c9-108">EXAMPLES</span></span>

### <span data-ttu-id="d51c9-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d51c9-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="d51c9-110">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="d51c9-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="d51c9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d51c9-111">PARAMETERS</span></span>

### <span data-ttu-id="d51c9-112">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d51c9-112">-DisplayName</span></span>
<span data-ttu-id="d51c9-113">Det namn som ska visas i adress boken för användaren.</span><span class="sxs-lookup"><span data-stu-id="d51c9-113">The name to display in the address book for the user.</span></span>
<span data-ttu-id="d51c9-114">exempel "Alex Wu".</span><span class="sxs-lookup"><span data-stu-id="d51c9-114">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="d51c9-115">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="d51c9-115">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="d51c9-116">Det måste anges om användaren måste ändra lösen ordet vid nästa lyckade inloggning (sant).</span><span class="sxs-lookup"><span data-stu-id="d51c9-116">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="d51c9-117">Standard beteende är (falskt) för att inte ändra lösen ordet vid nästa lyckade inloggning.</span><span class="sxs-lookup"><span data-stu-id="d51c9-117">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="d51c9-118">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="d51c9-118">-ImmutableId</span></span>
<span data-ttu-id="d51c9-119">Den måste anges bara om du använder en federerad domän som användarens huvud namn (UPN)-egenskap.</span><span class="sxs-lookup"><span data-stu-id="d51c9-119">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="d51c9-120">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="d51c9-120">-Password</span></span>
<span data-ttu-id="d51c9-121">Lösen ord för användaren.</span><span class="sxs-lookup"><span data-stu-id="d51c9-121">Password for the user.</span></span>
<span data-ttu-id="d51c9-122">Den måste uppfylla innehavarens komplexitets krav.</span><span class="sxs-lookup"><span data-stu-id="d51c9-122">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="d51c9-123">Vi rekommenderar att du anger ett starkt lösen ord.</span><span class="sxs-lookup"><span data-stu-id="d51c9-123">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="d51c9-124">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d51c9-124">-UserPrincipalName</span></span>
<span data-ttu-id="d51c9-125">Användarens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="d51c9-125">The user principal name.</span></span>
<span data-ttu-id="d51c9-126">Exempel-" someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="d51c9-126">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="d51c9-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d51c9-127">-Confirm</span></span>
<span data-ttu-id="d51c9-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d51c9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d51c9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d51c9-129">-WhatIf</span></span>
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

### <span data-ttu-id="d51c9-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d51c9-130">-DefaultProfile</span></span>
<span data-ttu-id="d51c9-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d51c9-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d51c9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d51c9-132">CommonParameters</span></span>
<span data-ttu-id="d51c9-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d51c9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d51c9-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d51c9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d51c9-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d51c9-135">INPUTS</span></span>

## <span data-ttu-id="d51c9-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d51c9-136">OUTPUTS</span></span>

### <span data-ttu-id="d51c9-137">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="d51c9-137">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="d51c9-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d51c9-138">NOTES</span></span>

## <span data-ttu-id="d51c9-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d51c9-139">RELATED LINKS</span></span>

[<span data-ttu-id="d51c9-140">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="d51c9-140">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="d51c9-141">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="d51c9-141">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="d51c9-142">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="d51c9-142">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
