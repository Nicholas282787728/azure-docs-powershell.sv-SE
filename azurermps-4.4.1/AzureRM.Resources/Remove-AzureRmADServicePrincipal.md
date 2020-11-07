---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 0a2350cf3e1c8619e1860a6a5c4a0832c978d9de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756856"
---
# <span data-ttu-id="cb6f7-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="cb6f7-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="cb6f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb6f7-102">SYNOPSIS</span></span>
<span data-ttu-id="cb6f7-103">Tar bort Azure Active Directory-huvudtjänsten.</span><span class="sxs-lookup"><span data-stu-id="cb6f7-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb6f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb6f7-104">SYNTAX</span></span>

```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb6f7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb6f7-105">DESCRIPTION</span></span>
<span data-ttu-id="cb6f7-106">Tar bort Azure Active Directory-huvudtjänsten.</span><span class="sxs-lookup"><span data-stu-id="cb6f7-106">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="cb6f7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb6f7-107">EXAMPLES</span></span>

### <span data-ttu-id="cb6f7-108">--------------------------Ta bort AAD-tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="cb6f7-108">--------------------------  Delete AAD service principal.</span></span>  --------------------------
```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="cb6f7-109">Tar bort angivet Azure Active Directory Service-huvudobjekt.</span><span class="sxs-lookup"><span data-stu-id="cb6f7-109">Deletes the given azure active directory service principal.</span></span>

## <span data-ttu-id="cb6f7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb6f7-110">PARAMETERS</span></span>

### <span data-ttu-id="cb6f7-111">-Force</span><span class="sxs-lookup"><span data-stu-id="cb6f7-111">-Force</span></span>
<span data-ttu-id="cb6f7-112">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="cb6f7-112">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="cb6f7-113">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cb6f7-113">-ObjectId</span></span>
<span data-ttu-id="cb6f7-114">Objekt-ID för det tjänst objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="cb6f7-114">The object id of the service principal to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb6f7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb6f7-115">-PassThru</span></span>
<span data-ttu-id="cb6f7-116">Om det anges returneras den borttagna tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="cb6f7-116">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="cb6f7-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cb6f7-117">-Confirm</span></span>
<span data-ttu-id="cb6f7-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cb6f7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb6f7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb6f7-119">-WhatIf</span></span>
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

### <span data-ttu-id="cb6f7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb6f7-120">-DefaultProfile</span></span>
<span data-ttu-id="cb6f7-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb6f7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb6f7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb6f7-122">CommonParameters</span></span>
<span data-ttu-id="cb6f7-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb6f7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb6f7-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb6f7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb6f7-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb6f7-125">INPUTS</span></span>

## <span data-ttu-id="cb6f7-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb6f7-126">OUTPUTS</span></span>

### <span data-ttu-id="cb6f7-127">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="cb6f7-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="cb6f7-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb6f7-128">NOTES</span></span>
<span data-ttu-id="cb6f7-129">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="cb6f7-129">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="cb6f7-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb6f7-130">RELATED LINKS</span></span>

[<span data-ttu-id="cb6f7-131">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="cb6f7-131">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="cb6f7-132">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="cb6f7-132">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="cb6f7-133">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="cb6f7-133">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="cb6f7-134">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="cb6f7-134">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="cb6f7-135">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="cb6f7-135">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
