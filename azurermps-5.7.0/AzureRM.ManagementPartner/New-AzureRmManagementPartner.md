---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393044
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/New-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/New-AzureRmManagementPartner.md
ms.openlocfilehash: 9a6d6d0d21a38ac5ff41460021287e0701de6057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581120"
---
# <span data-ttu-id="bdb15-101">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="bdb15-101">New-AzureRmManagementPartner</span></span>

## <span data-ttu-id="bdb15-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bdb15-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb15-103">Kopplar ett Microsoft Partner Network (MPN)-ID till den aktuella autentiserade användaren eller tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="bdb15-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdb15-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bdb15-104">SYNTAX</span></span>

```
New-AzureRmManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdb15-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bdb15-105">DESCRIPTION</span></span>
<span data-ttu-id="bdb15-106">Kopplar ett Microsoft Partner Network (MPN)-ID till den aktuella autentiserade användaren eller tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="bdb15-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="bdb15-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bdb15-107">EXAMPLES</span></span>

### <span data-ttu-id="bdb15-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bdb15-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="bdb15-109">Lägga till en hanterings partner</span><span class="sxs-lookup"><span data-stu-id="bdb15-109">Add a management partner</span></span> 

## <span data-ttu-id="bdb15-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bdb15-110">PARAMETERS</span></span>

### <span data-ttu-id="bdb15-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb15-111">-DefaultProfile</span></span>
<span data-ttu-id="bdb15-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bdb15-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdb15-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="bdb15-113">-PartnerId</span></span>
<span data-ttu-id="bdb15-114">ID för hanterings partnern är det ett 6 siffrors nummer</span><span class="sxs-lookup"><span data-stu-id="bdb15-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb15-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bdb15-115">-Confirm</span></span>
<span data-ttu-id="bdb15-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bdb15-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdb15-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdb15-117">-WhatIf</span></span>
<span data-ttu-id="bdb15-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bdb15-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdb15-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bdb15-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdb15-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb15-120">CommonParameters</span></span>
<span data-ttu-id="bdb15-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdb15-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb15-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdb15-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb15-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bdb15-123">INPUTS</span></span>

### <span data-ttu-id="bdb15-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="bdb15-124">None</span></span>

## <span data-ttu-id="bdb15-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bdb15-125">OUTPUTS</span></span>

### <span data-ttu-id="bdb15-126">Microsoft. Azure. commands. Resources. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="bdb15-126">Microsoft.Azure.Commands.Resources.PSManagementPartner</span></span>

## <span data-ttu-id="bdb15-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bdb15-127">NOTES</span></span>

## <span data-ttu-id="bdb15-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bdb15-128">RELATED LINKS</span></span>

[<span data-ttu-id="bdb15-129">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="bdb15-129">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="bdb15-130">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="bdb15-130">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)

[<span data-ttu-id="bdb15-131">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="bdb15-131">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
