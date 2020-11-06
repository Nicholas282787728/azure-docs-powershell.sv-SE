---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: 557cfcaefef1a85fe7ad0a8bd62f4ddbf0ecb6f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575668"
---
# <span data-ttu-id="b54fa-101">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="b54fa-101">Get-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="b54fa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b54fa-102">SYNOPSIS</span></span>
<span data-ttu-id="b54fa-103">Hämtar policyn för automatisk avslutning av ett labb i DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="b54fa-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b54fa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b54fa-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b54fa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b54fa-105">DESCRIPTION</span></span>
<span data-ttu-id="b54fa-106">Cmdleten **Get-AzureRmDtlAutoShutdownPolicy** hämtar den automatiska avslutnings principen för ett labb, vilket gör att du automatiskt kan stänga av alla virtuella datorer i ett labb under en viss tid.</span><span class="sxs-lookup"><span data-stu-id="b54fa-106">The **Get-AzureRmDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="b54fa-107">Cmdleten returnerar om principens status är aktive rad och den tid som du har angett för att stänga av virtuella laboratorie datorer automatiskt.</span><span class="sxs-lookup"><span data-stu-id="b54fa-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="b54fa-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b54fa-108">EXAMPLES</span></span>

## <span data-ttu-id="b54fa-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b54fa-109">PARAMETERS</span></span>

### <span data-ttu-id="b54fa-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b54fa-110">-DefaultProfile</span></span>
<span data-ttu-id="b54fa-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b54fa-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b54fa-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="b54fa-112">-LabName</span></span>
<span data-ttu-id="b54fa-113">Anger namnet på den Lab för vilken denna cmdlet får principen för automatisk avstängning.</span><span class="sxs-lookup"><span data-stu-id="b54fa-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b54fa-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b54fa-114">-ResourceGroupName</span></span>
<span data-ttu-id="b54fa-115">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="b54fa-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b54fa-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b54fa-116">CommonParameters</span></span>
<span data-ttu-id="b54fa-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b54fa-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b54fa-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b54fa-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b54fa-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b54fa-119">INPUTS</span></span>

### <span data-ttu-id="b54fa-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="b54fa-120">None</span></span>
<span data-ttu-id="b54fa-121">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b54fa-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b54fa-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b54fa-122">OUTPUTS</span></span>

### <span data-ttu-id="b54fa-123">Microsoft. Azure. commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="b54fa-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="b54fa-124">Denna cmdlet returnerar schemat som anger när laboratoriets virtuella datorer måste stängas av.</span><span class="sxs-lookup"><span data-stu-id="b54fa-124">This cmdlet returns the schedule which specifies when the lab's virtual machines must shut down.</span></span>

## <span data-ttu-id="b54fa-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b54fa-125">NOTES</span></span>

## <span data-ttu-id="b54fa-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b54fa-126">RELATED LINKS</span></span>

[<span data-ttu-id="b54fa-127">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="b54fa-127">Set-AzureRmDtlAutoShutdownPolicy</span></span>](./Set-AzureRmDtlAutoShutdownPolicy.md)


