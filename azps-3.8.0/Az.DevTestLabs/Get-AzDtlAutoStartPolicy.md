---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoStartPolicy.md
ms.openlocfilehash: 8b2269b46a120d34e696b2ee160aabceb0cba66c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090086"
---
# <span data-ttu-id="7f64c-101">Get-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="7f64c-101">Get-AzDtlAutoStartPolicy</span></span>

## <span data-ttu-id="7f64c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f64c-102">SYNOPSIS</span></span>
<span data-ttu-id="7f64c-103">Hämtar policyn för automatisk start för ett labb i DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="7f64c-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="7f64c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f64c-104">SYNTAX</span></span>

```
Get-AzDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f64c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f64c-105">DESCRIPTION</span></span>
<span data-ttu-id="7f64c-106">Cmdleten **Get-AzDtlAutoStartPolicy** för ett labb som schemalägger virtuella laboratorie datorer för automatisk start.</span><span class="sxs-lookup"><span data-stu-id="7f64c-106">The **Get-AzDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="7f64c-107">Cmdleten returnerar den aktiverade eller inaktiverade statusen för principen och de vecko dagar och den tid som du har angett för att tillåta att virtuella laboratorie datorer schemaläggs för automatisk start.</span><span class="sxs-lookup"><span data-stu-id="7f64c-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="7f64c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f64c-108">EXAMPLES</span></span>

## <span data-ttu-id="7f64c-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f64c-109">PARAMETERS</span></span>

### <span data-ttu-id="7f64c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f64c-110">-DefaultProfile</span></span>
<span data-ttu-id="7f64c-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7f64c-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f64c-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="7f64c-112">-LabName</span></span>
<span data-ttu-id="7f64c-113">Anger namnet på den Lab för vilken denna cmdlet ska starta principen för automatisk start.</span><span class="sxs-lookup"><span data-stu-id="7f64c-113">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

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

### <span data-ttu-id="7f64c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f64c-114">-ResourceGroupName</span></span>
<span data-ttu-id="7f64c-115">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="7f64c-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="7f64c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f64c-116">CommonParameters</span></span>
<span data-ttu-id="7f64c-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f64c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f64c-118">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f64c-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f64c-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f64c-119">INPUTS</span></span>

### <span data-ttu-id="7f64c-120">System. String</span><span class="sxs-lookup"><span data-stu-id="7f64c-120">System.String</span></span>

## <span data-ttu-id="7f64c-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f64c-121">OUTPUTS</span></span>

### <span data-ttu-id="7f64c-122">Microsoft. Azure. commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="7f64c-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="7f64c-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f64c-123">NOTES</span></span>

## <span data-ttu-id="7f64c-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f64c-124">RELATED LINKS</span></span>

[<span data-ttu-id="7f64c-125">Set-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="7f64c-125">Set-AzDtlAutoStartPolicy</span></span>](./Set-AzDtlAutoStartPolicy.md)


