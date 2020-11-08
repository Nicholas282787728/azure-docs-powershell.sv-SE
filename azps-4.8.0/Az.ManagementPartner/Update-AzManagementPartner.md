---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 326e16ff2f5bca8ca5ae987ebedf12cace87e11d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262186"
---
# <span data-ttu-id="dd5ff-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="dd5ff-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="dd5ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dd5ff-102">SYNOPSIS</span></span>
<span data-ttu-id="dd5ff-103">Uppdaterar det MPN (Microsoft Partner Network)-ID: t för den aktuella autentiserade användaren eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="dd5ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dd5ff-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd5ff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dd5ff-105">DESCRIPTION</span></span>
<span data-ttu-id="dd5ff-106">Uppdaterar det MPN (Microsoft Partner Network)-ID: t för den aktuella autentiserade användaren eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="dd5ff-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dd5ff-107">EXAMPLES</span></span>

### <span data-ttu-id="dd5ff-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dd5ff-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="dd5ff-109">Uppdatera hanterings partnern till en ny</span><span class="sxs-lookup"><span data-stu-id="dd5ff-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="dd5ff-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dd5ff-110">PARAMETERS</span></span>

### <span data-ttu-id="dd5ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd5ff-111">-DefaultProfile</span></span>
<span data-ttu-id="dd5ff-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd5ff-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="dd5ff-113">-PartnerId</span></span>
<span data-ttu-id="dd5ff-114">ID för hanterings partnern är det ett 6 siffrors nummer</span><span class="sxs-lookup"><span data-stu-id="dd5ff-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="dd5ff-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dd5ff-115">-Confirm</span></span>
<span data-ttu-id="dd5ff-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd5ff-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd5ff-117">-WhatIf</span></span>
<span data-ttu-id="dd5ff-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd5ff-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd5ff-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd5ff-120">CommonParameters</span></span>
<span data-ttu-id="dd5ff-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd5ff-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd5ff-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd5ff-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd5ff-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dd5ff-123">INPUTS</span></span>

### <span data-ttu-id="dd5ff-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="dd5ff-124">None</span></span>

## <span data-ttu-id="dd5ff-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dd5ff-125">OUTPUTS</span></span>

### <span data-ttu-id="dd5ff-126">Microsoft. Azure. commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="dd5ff-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="dd5ff-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dd5ff-127">NOTES</span></span>

## <span data-ttu-id="dd5ff-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dd5ff-128">RELATED LINKS</span></span>

[<span data-ttu-id="dd5ff-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="dd5ff-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="dd5ff-130">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="dd5ff-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="dd5ff-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="dd5ff-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)