---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: 4717fa187a8bd8234cd786ff5c6ad6d1678696b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756972"
---
# <span data-ttu-id="3825c-101">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="3825c-101">Get-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="3825c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3825c-102">SYNOPSIS</span></span>
<span data-ttu-id="3825c-103">Hämtar policyn för automatisk avslutning av ett labb i DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="3825c-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3825c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3825c-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3825c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3825c-105">DESCRIPTION</span></span>
<span data-ttu-id="3825c-106">Cmdleten **Get-AzureRmDtlAutoShutdownPolicy** hämtar den automatiska avslutnings principen för ett labb, vilket gör att du automatiskt kan stänga av alla virtuella datorer i ett labb under en viss tid.</span><span class="sxs-lookup"><span data-stu-id="3825c-106">The **Get-AzureRmDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="3825c-107">Cmdleten returnerar om principens status är aktive rad och den tid som du har angett för att stänga av virtuella laboratorie datorer automatiskt.</span><span class="sxs-lookup"><span data-stu-id="3825c-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="3825c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3825c-108">EXAMPLES</span></span>

## <span data-ttu-id="3825c-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3825c-109">PARAMETERS</span></span>

### <span data-ttu-id="3825c-110">-LabName</span><span class="sxs-lookup"><span data-stu-id="3825c-110">-LabName</span></span>
<span data-ttu-id="3825c-111">Anger namnet på den Lab för vilken denna cmdlet får principen för automatisk avstängning.</span><span class="sxs-lookup"><span data-stu-id="3825c-111">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3825c-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3825c-112">-ResourceGroupName</span></span>
<span data-ttu-id="3825c-113">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="3825c-113">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3825c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3825c-114">-DefaultProfile</span></span>
<span data-ttu-id="3825c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3825c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3825c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3825c-116">CommonParameters</span></span>
<span data-ttu-id="3825c-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3825c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3825c-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3825c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3825c-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3825c-119">INPUTS</span></span>

## <span data-ttu-id="3825c-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3825c-120">OUTPUTS</span></span>

### <span data-ttu-id="3825c-121">Microsoft. Azure. commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="3825c-121">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="3825c-122">Denna cmdlet returnerar schemat som anger när laboratoriets virtuella datorer måste stängas av.</span><span class="sxs-lookup"><span data-stu-id="3825c-122">This cmdlet returns the schedule which specifies when the lab's virtual machines must shut down.</span></span>

## <span data-ttu-id="3825c-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3825c-123">NOTES</span></span>

## <span data-ttu-id="3825c-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3825c-124">RELATED LINKS</span></span>

[<span data-ttu-id="3825c-125">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="3825c-125">Set-AzureRmDtlAutoShutdownPolicy</span></span>](./Set-AzureRmDtlAutoShutdownPolicy.md)


