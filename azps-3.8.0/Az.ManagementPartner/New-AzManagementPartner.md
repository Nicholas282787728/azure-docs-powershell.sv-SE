---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/new-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
ms.openlocfilehash: 9e6c56fa48b71e2571b7702e170bdc3e9e41f3aa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926046"
---
# <span data-ttu-id="8cdc0-101">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="8cdc0-101">New-AzManagementPartner</span></span>

## <span data-ttu-id="8cdc0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8cdc0-102">SYNOPSIS</span></span>
<span data-ttu-id="8cdc0-103">Kopplar ett Microsoft Partner Network (MPN)-ID till den aktuella autentiserade användaren eller tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="8cdc0-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="8cdc0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8cdc0-104">SYNTAX</span></span>

```
New-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8cdc0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8cdc0-105">DESCRIPTION</span></span>
<span data-ttu-id="8cdc0-106">Kopplar ett Microsoft Partner Network (MPN)-ID till den aktuella autentiserade användaren eller tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="8cdc0-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="8cdc0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8cdc0-107">EXAMPLES</span></span>

### <span data-ttu-id="8cdc0-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8cdc0-108">Example 1</span></span>
```powershell
PS C:\> New-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="8cdc0-109">Lägga till en hanterings partner</span><span class="sxs-lookup"><span data-stu-id="8cdc0-109">Add a management partner</span></span>

## <span data-ttu-id="8cdc0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8cdc0-110">PARAMETERS</span></span>

### <span data-ttu-id="8cdc0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cdc0-111">-DefaultProfile</span></span>
<span data-ttu-id="8cdc0-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8cdc0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cdc0-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="8cdc0-113">-PartnerId</span></span>
<span data-ttu-id="8cdc0-114">ID för hanterings partnern är det ett 6 siffrors nummer</span><span class="sxs-lookup"><span data-stu-id="8cdc0-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="8cdc0-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8cdc0-115">-Confirm</span></span>
<span data-ttu-id="8cdc0-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8cdc0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cdc0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cdc0-117">-WhatIf</span></span>
<span data-ttu-id="8cdc0-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8cdc0-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cdc0-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8cdc0-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cdc0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cdc0-120">CommonParameters</span></span>
<span data-ttu-id="8cdc0-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cdc0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cdc0-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cdc0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cdc0-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8cdc0-123">INPUTS</span></span>

### <span data-ttu-id="8cdc0-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="8cdc0-124">None</span></span>

## <span data-ttu-id="8cdc0-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8cdc0-125">OUTPUTS</span></span>

### <span data-ttu-id="8cdc0-126">Microsoft. Azure. commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="8cdc0-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="8cdc0-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8cdc0-127">NOTES</span></span>

## <span data-ttu-id="8cdc0-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8cdc0-128">RELATED LINKS</span></span>

[<span data-ttu-id="8cdc0-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="8cdc0-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="8cdc0-130">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="8cdc0-130">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="8cdc0-131">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="8cdc0-131">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)