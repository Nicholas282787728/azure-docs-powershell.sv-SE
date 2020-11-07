---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: c61739c3bd80c5c5c15c7e10d8a787f45c44ec69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755763"
---
# <span data-ttu-id="d14ba-101">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="d14ba-101">Get-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="d14ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d14ba-102">SYNOPSIS</span></span>
<span data-ttu-id="d14ba-103">Hämtar policyn för automatisk start för ett labb i DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="d14ba-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d14ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d14ba-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d14ba-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d14ba-105">DESCRIPTION</span></span>
<span data-ttu-id="d14ba-106">Cmdleten **Get-AzureRmDtlAutoStartPolicy** för ett labb som schemalägger virtuella laboratorie datorer för automatisk start.</span><span class="sxs-lookup"><span data-stu-id="d14ba-106">The **Get-AzureRmDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="d14ba-107">Cmdleten returnerar den aktiverade eller inaktiverade statusen för principen och de vecko dagar och den tid som du har angett för att tillåta att virtuella laboratorie datorer schemaläggs för automatisk start.</span><span class="sxs-lookup"><span data-stu-id="d14ba-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="d14ba-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d14ba-108">EXAMPLES</span></span>

## <span data-ttu-id="d14ba-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d14ba-109">PARAMETERS</span></span>

### <span data-ttu-id="d14ba-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d14ba-110">-DefaultProfile</span></span>
<span data-ttu-id="d14ba-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d14ba-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d14ba-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="d14ba-112">-LabName</span></span>
<span data-ttu-id="d14ba-113">Anger namnet på den Lab för vilken denna cmdlet ska starta principen för automatisk start.</span><span class="sxs-lookup"><span data-stu-id="d14ba-113">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

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

### <span data-ttu-id="d14ba-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d14ba-114">-ResourceGroupName</span></span>
<span data-ttu-id="d14ba-115">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="d14ba-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="d14ba-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d14ba-116">CommonParameters</span></span>
<span data-ttu-id="d14ba-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d14ba-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d14ba-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d14ba-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d14ba-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d14ba-119">INPUTS</span></span>

### <span data-ttu-id="d14ba-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="d14ba-120">None</span></span>
<span data-ttu-id="d14ba-121">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d14ba-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d14ba-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d14ba-122">OUTPUTS</span></span>

### <span data-ttu-id="d14ba-123">Microsoft. Azure. commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="d14ba-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="d14ba-124">Denna cmdlet returnerar schemat som anger när laboratoriets virtuella datorer måste startas.</span><span class="sxs-lookup"><span data-stu-id="d14ba-124">This cmdlet returns the schedule that specifies when the lab's virtual machines must be started.</span></span>

## <span data-ttu-id="d14ba-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d14ba-125">NOTES</span></span>

## <span data-ttu-id="d14ba-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d14ba-126">RELATED LINKS</span></span>

[<span data-ttu-id="d14ba-127">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="d14ba-127">Set-AzureRmDtlAutoStartPolicy</span></span>](./Set-AzureRmDtlAutoStartPolicy.md)


