---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1f2c7e653e96f697a714fef9f7b56c70240f0456
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324869"
---
# <span data-ttu-id="3be8f-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3be8f-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="3be8f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3be8f-102">SYNOPSIS</span></span>
<span data-ttu-id="3be8f-103">Testar om Stream Analytics kan ansluta till en funktion.</span><span class="sxs-lookup"><span data-stu-id="3be8f-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="3be8f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3be8f-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3be8f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3be8f-105">DESCRIPTION</span></span>
<span data-ttu-id="3be8f-106">**Test-AzStreamAnalyticsFunction** cmdlet testar om Azure Stream Analytics kan ansluta till en funktion.</span><span class="sxs-lookup"><span data-stu-id="3be8f-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="3be8f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3be8f-107">EXAMPLES</span></span>

### <span data-ttu-id="3be8f-108">Exempel 1: testa en Stream Analytics-funktion</span><span class="sxs-lookup"><span data-stu-id="3be8f-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="3be8f-109">Det här kommandot testar anslutnings statusen för funktionen som heter ScoreTweet i jobbet med namnet StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="3be8f-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="3be8f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3be8f-110">PARAMETERS</span></span>

### <span data-ttu-id="3be8f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3be8f-111">-DefaultProfile</span></span>
<span data-ttu-id="3be8f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3be8f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3be8f-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="3be8f-113">-JobName</span></span>
<span data-ttu-id="3be8f-114">Anger namnet på det Stream analys jobb som en funktion tillhör.</span><span class="sxs-lookup"><span data-stu-id="3be8f-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="3be8f-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="3be8f-115">-Name</span></span>
<span data-ttu-id="3be8f-116">Anger namnet på den ström analys funktion som denna cmdlet testar.</span><span class="sxs-lookup"><span data-stu-id="3be8f-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3be8f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3be8f-117">-ResourceGroupName</span></span>
<span data-ttu-id="3be8f-118">Anger namnet på den resurs grupp som en Stream Analytics-funktion tillhör.</span><span class="sxs-lookup"><span data-stu-id="3be8f-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="3be8f-119">Denna cmdlet testar en funktion i resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="3be8f-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3be8f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3be8f-120">CommonParameters</span></span>
<span data-ttu-id="3be8f-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3be8f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3be8f-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3be8f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3be8f-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3be8f-123">INPUTS</span></span>

### <span data-ttu-id="3be8f-124">System. String</span><span class="sxs-lookup"><span data-stu-id="3be8f-124">System.String</span></span>

## <span data-ttu-id="3be8f-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3be8f-125">OUTPUTS</span></span>

### <span data-ttu-id="3be8f-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3be8f-126">System.Boolean</span></span>

## <span data-ttu-id="3be8f-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3be8f-127">NOTES</span></span>

## <span data-ttu-id="3be8f-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3be8f-128">RELATED LINKS</span></span>

[<span data-ttu-id="3be8f-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3be8f-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="3be8f-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3be8f-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="3be8f-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3be8f-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

