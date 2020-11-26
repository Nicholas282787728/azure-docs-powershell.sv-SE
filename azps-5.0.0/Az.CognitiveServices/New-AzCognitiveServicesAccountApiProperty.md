---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 97cf393d0d95dbc9ecfec06f53795713f59aecbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321780"
---
# <span data-ttu-id="7be06-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="7be06-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="7be06-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7be06-102">SYNOPSIS</span></span>
<span data-ttu-id="7be06-103">Skapa en ny instans av ett konto för kognitiva ApiProperties</span><span class="sxs-lookup"><span data-stu-id="7be06-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="7be06-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7be06-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7be06-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7be06-105">DESCRIPTION</span></span>
<span data-ttu-id="7be06-106">Skapa en ny instans av ett konto för kognitiva ApiProperties.</span><span class="sxs-lookup"><span data-stu-id="7be06-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="7be06-107">ApiProperties kan användas när du skapar ett nytt konto eller uppdaterar ett befintligt konto.</span><span class="sxs-lookup"><span data-stu-id="7be06-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="7be06-108">ApiProperties är obligatoriskt för vissa konto typer.</span><span class="sxs-lookup"><span data-stu-id="7be06-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="7be06-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7be06-109">EXAMPLES</span></span>

### <span data-ttu-id="7be06-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7be06-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="7be06-111">Ovan skapas ett QnAMaker-konto med API-egenskapen "QnaRuntimeEndpoint".</span><span class="sxs-lookup"><span data-stu-id="7be06-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="7be06-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7be06-112">PARAMETERS</span></span>

### <span data-ttu-id="7be06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7be06-113">-DefaultProfile</span></span>
<span data-ttu-id="7be06-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7be06-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be06-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7be06-115">-Confirm</span></span>
<span data-ttu-id="7be06-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7be06-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7be06-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7be06-117">-WhatIf</span></span>
<span data-ttu-id="7be06-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7be06-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7be06-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7be06-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7be06-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7be06-120">CommonParameters</span></span>
<span data-ttu-id="7be06-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7be06-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7be06-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7be06-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7be06-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7be06-123">INPUTS</span></span>

### <span data-ttu-id="7be06-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="7be06-124">None</span></span>

## <span data-ttu-id="7be06-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7be06-125">OUTPUTS</span></span>

### <span data-ttu-id="7be06-126">Microsoft. Azure. Management. CognitiveServices. Models. CognitiveServicesAccountApiProperties</span><span class="sxs-lookup"><span data-stu-id="7be06-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="7be06-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7be06-127">NOTES</span></span>

## <span data-ttu-id="7be06-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7be06-128">RELATED LINKS</span></span>