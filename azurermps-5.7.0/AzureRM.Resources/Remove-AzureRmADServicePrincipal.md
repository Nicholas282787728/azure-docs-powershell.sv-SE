---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 8bf47d9753d7cd8d97c14eb2ec1ac7c6384f7c1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756452"
---
# <span data-ttu-id="25853-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="25853-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="25853-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25853-102">SYNOPSIS</span></span>
<span data-ttu-id="25853-103">Tar bort Azure Active Directory-huvudtjänsten.</span><span class="sxs-lookup"><span data-stu-id="25853-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25853-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25853-104">SYNTAX</span></span>

```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25853-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25853-105">DESCRIPTION</span></span>
<span data-ttu-id="25853-106">Tar bort Azure Active Directory-huvudtjänsten.</span><span class="sxs-lookup"><span data-stu-id="25853-106">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="25853-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25853-107">EXAMPLES</span></span>

### <span data-ttu-id="25853-108">Ta bort AAD-tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="25853-108">Delete AAD service principal.</span></span>
```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="25853-109">Tar bort angivet Azure Active Directory Service-huvudobjekt.</span><span class="sxs-lookup"><span data-stu-id="25853-109">Deletes the given azure active directory service principal.</span></span>

## <span data-ttu-id="25853-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25853-110">PARAMETERS</span></span>

### <span data-ttu-id="25853-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25853-111">-DefaultProfile</span></span>
<span data-ttu-id="25853-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="25853-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25853-113">-Force</span><span class="sxs-lookup"><span data-stu-id="25853-113">-Force</span></span>
<span data-ttu-id="25853-114">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="25853-114">{{Fill Force Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25853-115">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="25853-115">-ObjectId</span></span>
<span data-ttu-id="25853-116">Objekt-ID för det tjänst objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="25853-116">The object id of the service principal to delete.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25853-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25853-117">-PassThru</span></span>
<span data-ttu-id="25853-118">Om det anges returneras den borttagna tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="25853-118">If specified, returns the deleted service principal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25853-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="25853-119">-Confirm</span></span>
<span data-ttu-id="25853-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="25853-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25853-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25853-121">-WhatIf</span></span>
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

### <span data-ttu-id="25853-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25853-122">CommonParameters</span></span>
<span data-ttu-id="25853-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25853-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25853-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25853-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25853-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25853-125">INPUTS</span></span>

### <span data-ttu-id="25853-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="25853-126">None</span></span>
<span data-ttu-id="25853-127">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="25853-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="25853-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25853-128">OUTPUTS</span></span>

### <span data-ttu-id="25853-129">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="25853-129">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="25853-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25853-130">NOTES</span></span>
<span data-ttu-id="25853-131">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="25853-131">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="25853-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25853-132">RELATED LINKS</span></span>

[<span data-ttu-id="25853-133">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="25853-133">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="25853-134">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="25853-134">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="25853-135">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="25853-135">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="25853-136">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="25853-136">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="25853-137">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="25853-137">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
