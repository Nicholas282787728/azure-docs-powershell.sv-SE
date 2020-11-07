---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393054
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Update-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Update-AzureRmManagementPartner.md
ms.openlocfilehash: 9d1694cdde3edd94112fc5b1960fd870b842d6e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756274"
---
# <span data-ttu-id="42464-101">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="42464-101">Update-AzureRmManagementPartner</span></span>

## <span data-ttu-id="42464-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42464-102">SYNOPSIS</span></span>
<span data-ttu-id="42464-103">Uppdaterar det MPN (Microsoft Partner Network)-ID: t för den aktuella autentiserade användaren eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="42464-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42464-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42464-104">SYNTAX</span></span>

```
Update-AzureRmManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42464-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42464-105">DESCRIPTION</span></span>
<span data-ttu-id="42464-106">Uppdaterar det MPN (Microsoft Partner Network)-ID: t för den aktuella autentiserade användaren eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="42464-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="42464-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42464-107">EXAMPLES</span></span>

### <span data-ttu-id="42464-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="42464-108">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="42464-109">Uppdatera hanterings partnern till en ny</span><span class="sxs-lookup"><span data-stu-id="42464-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="42464-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42464-110">PARAMETERS</span></span>

### <span data-ttu-id="42464-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42464-111">-DefaultProfile</span></span>
<span data-ttu-id="42464-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="42464-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42464-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="42464-113">-PartnerId</span></span>
<span data-ttu-id="42464-114">ID för hanterings partnern är det ett 6 siffrors nummer</span><span class="sxs-lookup"><span data-stu-id="42464-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="42464-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="42464-115">-Confirm</span></span>
<span data-ttu-id="42464-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="42464-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42464-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42464-117">-WhatIf</span></span>
<span data-ttu-id="42464-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="42464-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42464-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="42464-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42464-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42464-120">CommonParameters</span></span>
<span data-ttu-id="42464-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42464-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42464-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42464-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42464-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42464-123">INPUTS</span></span>

### <span data-ttu-id="42464-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="42464-124">None</span></span>

## <span data-ttu-id="42464-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42464-125">OUTPUTS</span></span>

### <span data-ttu-id="42464-126">Microsoft. Azure. commands. Resources. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="42464-126">Microsoft.Azure.Commands.Resources.PSManagementPartner</span></span>

## <span data-ttu-id="42464-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42464-127">NOTES</span></span>

## <span data-ttu-id="42464-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42464-128">RELATED LINKS</span></span>

[<span data-ttu-id="42464-129">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="42464-129">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="42464-130">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="42464-130">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="42464-131">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="42464-131">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)
