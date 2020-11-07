---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: a2f577286a411287886c27863eb72e574b771bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756318"
---
# <span data-ttu-id="0dd10-101">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="0dd10-101">Test-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="0dd10-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0dd10-102">SYNOPSIS</span></span>
<span data-ttu-id="0dd10-103">Testar om Stream Analytics kan ansluta till en funktion.</span><span class="sxs-lookup"><span data-stu-id="0dd10-103">Tests whether Stream Analytics can connect to a function.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0dd10-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0dd10-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0dd10-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0dd10-105">DESCRIPTION</span></span>
<span data-ttu-id="0dd10-106">**Test-AzureRmStreamAnalyticsFunction** cmdlet testar om Azure Stream Analytics kan ansluta till en funktion.</span><span class="sxs-lookup"><span data-stu-id="0dd10-106">The **Test-AzureRmStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="0dd10-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0dd10-107">EXAMPLES</span></span>

### <span data-ttu-id="0dd10-108">Exempel 1: testa en Stream Analytics-funktion</span><span class="sxs-lookup"><span data-stu-id="0dd10-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="0dd10-109">Det här kommandot testar anslutnings statusen för funktionen som heter ScoreTweet i jobbet med namnet StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="0dd10-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="0dd10-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0dd10-110">PARAMETERS</span></span>

### <span data-ttu-id="0dd10-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="0dd10-111">-JobName</span></span>
<span data-ttu-id="0dd10-112">Anger namnet på det Stream analys jobb som en funktion tillhör.</span><span class="sxs-lookup"><span data-stu-id="0dd10-112">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="0dd10-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="0dd10-113">-Name</span></span>
<span data-ttu-id="0dd10-114">Anger namnet på den ström analys funktion som denna cmdlet testar.</span><span class="sxs-lookup"><span data-stu-id="0dd10-114">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="0dd10-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dd10-115">-ResourceGroupName</span></span>
<span data-ttu-id="0dd10-116">Anger namnet på den resurs grupp som en Stream Analytics-funktion tillhör.</span><span class="sxs-lookup"><span data-stu-id="0dd10-116">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="0dd10-117">Denna cmdlet testar en funktion i resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="0dd10-117">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0dd10-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dd10-118">-DefaultProfile</span></span>
<span data-ttu-id="0dd10-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0dd10-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0dd10-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dd10-120">CommonParameters</span></span>
<span data-ttu-id="0dd10-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dd10-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dd10-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dd10-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dd10-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0dd10-123">INPUTS</span></span>

## <span data-ttu-id="0dd10-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0dd10-124">OUTPUTS</span></span>

### <span data-ttu-id="0dd10-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="0dd10-125">System.Object</span></span>

## <span data-ttu-id="0dd10-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0dd10-126">NOTES</span></span>

## <span data-ttu-id="0dd10-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0dd10-127">RELATED LINKS</span></span>

[<span data-ttu-id="0dd10-128">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="0dd10-128">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="0dd10-129">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="0dd10-129">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="0dd10-130">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="0dd10-130">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)


