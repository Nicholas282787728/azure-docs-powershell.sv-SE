---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: efe948e2676b44a70917efb43e901f8848dec0e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576296"
---
# <span data-ttu-id="257bb-101">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="257bb-101">Get-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="257bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="257bb-102">SYNOPSIS</span></span>
<span data-ttu-id="257bb-103">Hämtar policyn för automatisk start för ett labb i DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="257bb-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="257bb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="257bb-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="257bb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="257bb-105">DESCRIPTION</span></span>
<span data-ttu-id="257bb-106">Cmdleten **Get-AzureRmDtlAutoStartPolicy** för ett labb som schemalägger virtuella laboratorie datorer för automatisk start.</span><span class="sxs-lookup"><span data-stu-id="257bb-106">The **Get-AzureRmDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="257bb-107">Cmdleten returnerar den aktiverade eller inaktiverade statusen för principen och de vecko dagar och den tid som du har angett för att tillåta att virtuella laboratorie datorer schemaläggs för automatisk start.</span><span class="sxs-lookup"><span data-stu-id="257bb-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="257bb-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="257bb-108">EXAMPLES</span></span>

## <span data-ttu-id="257bb-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="257bb-109">PARAMETERS</span></span>

### <span data-ttu-id="257bb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="257bb-110">-DefaultProfile</span></span>
<span data-ttu-id="257bb-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="257bb-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="257bb-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="257bb-112">-LabName</span></span>
<span data-ttu-id="257bb-113">Anger namnet på den Lab för vilken denna cmdlet ska starta principen för automatisk start.</span><span class="sxs-lookup"><span data-stu-id="257bb-113">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

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

### <span data-ttu-id="257bb-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="257bb-114">-ResourceGroupName</span></span>
<span data-ttu-id="257bb-115">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="257bb-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="257bb-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="257bb-116">CommonParameters</span></span>
<span data-ttu-id="257bb-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="257bb-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="257bb-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="257bb-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="257bb-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="257bb-119">INPUTS</span></span>

### <span data-ttu-id="257bb-120">System. String</span><span class="sxs-lookup"><span data-stu-id="257bb-120">System.String</span></span>

## <span data-ttu-id="257bb-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="257bb-121">OUTPUTS</span></span>

### <span data-ttu-id="257bb-122">Microsoft. Azure. commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="257bb-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="257bb-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="257bb-123">NOTES</span></span>

## <span data-ttu-id="257bb-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="257bb-124">RELATED LINKS</span></span>

[<span data-ttu-id="257bb-125">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="257bb-125">Set-AzureRmDtlAutoStartPolicy</span></span>](./Set-AzureRmDtlAutoStartPolicy.md)


