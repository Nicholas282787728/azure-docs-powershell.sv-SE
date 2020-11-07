---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 326e16ff2f5bca8ca5ae987ebedf12cace87e11d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926038"
---
# <span data-ttu-id="b6de2-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b6de2-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="b6de2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6de2-102">SYNOPSIS</span></span>
<span data-ttu-id="b6de2-103">Uppdaterar det MPN (Microsoft Partner Network)-ID: t för den aktuella autentiserade användaren eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="b6de2-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="b6de2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6de2-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6de2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6de2-105">DESCRIPTION</span></span>
<span data-ttu-id="b6de2-106">Uppdaterar det MPN (Microsoft Partner Network)-ID: t för den aktuella autentiserade användaren eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="b6de2-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="b6de2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6de2-107">EXAMPLES</span></span>

### <span data-ttu-id="b6de2-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b6de2-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="b6de2-109">Uppdatera hanterings partnern till en ny</span><span class="sxs-lookup"><span data-stu-id="b6de2-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="b6de2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6de2-110">PARAMETERS</span></span>

### <span data-ttu-id="b6de2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6de2-111">-DefaultProfile</span></span>
<span data-ttu-id="b6de2-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6de2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6de2-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="b6de2-113">-PartnerId</span></span>
<span data-ttu-id="b6de2-114">ID för hanterings partnern är det ett 6 siffrors nummer</span><span class="sxs-lookup"><span data-stu-id="b6de2-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6de2-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b6de2-115">-Confirm</span></span>
<span data-ttu-id="b6de2-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b6de2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6de2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6de2-117">-WhatIf</span></span>
<span data-ttu-id="b6de2-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b6de2-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6de2-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b6de2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6de2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6de2-120">CommonParameters</span></span>
<span data-ttu-id="b6de2-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6de2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6de2-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6de2-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6de2-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6de2-123">INPUTS</span></span>

### <span data-ttu-id="b6de2-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="b6de2-124">None</span></span>

## <span data-ttu-id="b6de2-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6de2-125">OUTPUTS</span></span>

### <span data-ttu-id="b6de2-126">Microsoft. Azure. commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b6de2-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="b6de2-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6de2-127">NOTES</span></span>

## <span data-ttu-id="b6de2-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6de2-128">RELATED LINKS</span></span>

[<span data-ttu-id="b6de2-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b6de2-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="b6de2-130">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b6de2-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="b6de2-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b6de2-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)