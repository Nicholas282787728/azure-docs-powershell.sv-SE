---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: de0c1f8fa66b195452d7f2c9447189b4e925136b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582423"
---
# <span data-ttu-id="1914b-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="1914b-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="1914b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1914b-102">SYNOPSIS</span></span>
<span data-ttu-id="1914b-103">Tar bort en varnings regel.</span><span class="sxs-lookup"><span data-stu-id="1914b-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1914b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1914b-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroup <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1914b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1914b-105">DESCRIPTION</span></span>
<span data-ttu-id="1914b-106">Cmdleten **Remove-AzureRmAlertRule** tar bort en notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="1914b-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="1914b-107">Du måste ange namnet på notifieringsregeln och resurs gruppen som den har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="1914b-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>

## <span data-ttu-id="1914b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1914b-108">EXAMPLES</span></span>

### <span data-ttu-id="1914b-109">Exempel 1: ta bort en notifieringsregel</span><span class="sxs-lookup"><span data-stu-id="1914b-109">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="1914b-110">Med det här kommandot tas notifieringsregeln bort med namnet avisering-7da64548-214d-42CA-b12b-b245bb8f0ac8 i resurs gruppens standard webb-centrala.</span><span class="sxs-lookup"><span data-stu-id="1914b-110">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="1914b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1914b-111">PARAMETERS</span></span>

### <span data-ttu-id="1914b-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="1914b-112">-Name</span></span>
<span data-ttu-id="1914b-113">Anger namnet på den notifieringsregel som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="1914b-113">Specifies the name of the alert rule to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1914b-114">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1914b-114">-ResourceGroup</span></span>
<span data-ttu-id="1914b-115">Anger namnet på resurs gruppen för notifieringsregeln.</span><span class="sxs-lookup"><span data-stu-id="1914b-115">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1914b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1914b-116">-DefaultProfile</span></span>
<span data-ttu-id="1914b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1914b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1914b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1914b-118">CommonParameters</span></span>
<span data-ttu-id="1914b-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1914b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1914b-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1914b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1914b-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1914b-121">INPUTS</span></span>

## <span data-ttu-id="1914b-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1914b-122">OUTPUTS</span></span>

### <span data-ttu-id="1914b-123">System. Collections. Generic. list ' 1 [Microsoft. Azure. AzureOperationResponse]</span><span class="sxs-lookup"><span data-stu-id="1914b-123">System.Collections.Generic.List\`1[Microsoft.Azure.AzureOperationResponse]</span></span>

## <span data-ttu-id="1914b-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1914b-124">NOTES</span></span>

## <span data-ttu-id="1914b-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1914b-125">RELATED LINKS</span></span>

[<span data-ttu-id="1914b-126">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="1914b-126">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="1914b-127">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="1914b-127">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="1914b-128">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="1914b-128">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="1914b-129">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="1914b-129">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="1914b-130">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="1914b-130">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


