---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: e13b90da8e1901faf0b18eb6ebf3cc78ce1bbcda
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101484"
---
# <span data-ttu-id="20009-101">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="20009-101">Get-AzHDInsightProperty</span></span>

## <span data-ttu-id="20009-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20009-102">SYNOPSIS</span></span>
<span data-ttu-id="20009-103">Hämtar egenskaper för HDInsight-tjänsten, till exempel tillgängliga platser och kapacitet.</span><span class="sxs-lookup"><span data-stu-id="20009-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

## <span data-ttu-id="20009-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20009-104">SYNTAX</span></span>

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20009-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20009-105">DESCRIPTION</span></span>
<span data-ttu-id="20009-106">Cmdleten **Get-AzHDInsightProperty** hämtar egenskaper som är specifika för Azure HDInsight, till exempel listan över tillgängliga platser, HDInsight-kluster versioner och tillgänglig beräknings kapacitet.</span><span class="sxs-lookup"><span data-stu-id="20009-106">The **Get-AzHDInsightProperty** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="20009-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20009-107">EXAMPLES</span></span>

### <span data-ttu-id="20009-108">Exempel 1: Hämta egenskaperna för ett Azure HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="20009-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

<span data-ttu-id="20009-109">Det här kommandot får egenskaper från en HDInsight-tjänst från platsen östra USA 2.</span><span class="sxs-lookup"><span data-stu-id="20009-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="20009-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20009-110">PARAMETERS</span></span>

### <span data-ttu-id="20009-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20009-111">-DefaultProfile</span></span>
<span data-ttu-id="20009-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="20009-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20009-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="20009-113">-Location</span></span>
<span data-ttu-id="20009-114">Anger platsen för vilken metabasegenskaper-egenskaper hämtas.</span><span class="sxs-lookup"><span data-stu-id="20009-114">Specifies the location for which to fetch HDInsight properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20009-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20009-115">CommonParameters</span></span>
<span data-ttu-id="20009-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20009-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20009-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20009-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20009-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20009-118">INPUTS</span></span>

### <span data-ttu-id="20009-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="20009-119">None</span></span>
## <span data-ttu-id="20009-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20009-120">OUTPUTS</span></span>

### <span data-ttu-id="20009-121">Microsoft. Azure. Management. HDInsight. Models. AzureHDInsightCapabilities</span><span class="sxs-lookup"><span data-stu-id="20009-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span></span>
## <span data-ttu-id="20009-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20009-122">NOTES</span></span>

## <span data-ttu-id="20009-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20009-123">RELATED LINKS</span></span>
