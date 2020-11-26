---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: 1031c9c8828969d16097953aa7440e2c8c0a8c1b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102790"
---
# <span data-ttu-id="5e749-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="5e749-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="5e749-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e749-102">SYNOPSIS</span></span>
<span data-ttu-id="5e749-103">Hämtar MPN-ID för den aktuella autentiserade användaren eller tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="5e749-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="5e749-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e749-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e749-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e749-105">DESCRIPTION</span></span>
<span data-ttu-id="5e749-106">Hämtar MPN-ID för den aktuella autentiserade användaren eller tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="5e749-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="5e749-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e749-107">EXAMPLES</span></span>

### <span data-ttu-id="5e749-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5e749-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="5e749-109">Skaffa aktuellt Management partner-ID</span><span class="sxs-lookup"><span data-stu-id="5e749-109">Get the current management partner id</span></span>

### <span data-ttu-id="5e749-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5e749-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="5e749-111">Skaffa det aktuella Management partner-ID: t med ett partner-ID, om de inte stämmer överens</span><span class="sxs-lookup"><span data-stu-id="5e749-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="5e749-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e749-112">PARAMETERS</span></span>

### <span data-ttu-id="5e749-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e749-113">-DefaultProfile</span></span>
<span data-ttu-id="5e749-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5e749-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e749-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="5e749-115">-PartnerId</span></span>
<span data-ttu-id="5e749-116">ID för hanterings partnern är det ett 6 siffrors nummer</span><span class="sxs-lookup"><span data-stu-id="5e749-116">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e749-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e749-117">CommonParameters</span></span>
<span data-ttu-id="5e749-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e749-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e749-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e749-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e749-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e749-120">INPUTS</span></span>

### <span data-ttu-id="5e749-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="5e749-121">None</span></span>

## <span data-ttu-id="5e749-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e749-122">OUTPUTS</span></span>

### <span data-ttu-id="5e749-123">Microsoft. Azure. commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="5e749-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="5e749-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e749-124">NOTES</span></span>

## <span data-ttu-id="5e749-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e749-125">RELATED LINKS</span></span>

[<span data-ttu-id="5e749-126">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="5e749-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="5e749-127">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="5e749-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="5e749-128">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="5e749-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)