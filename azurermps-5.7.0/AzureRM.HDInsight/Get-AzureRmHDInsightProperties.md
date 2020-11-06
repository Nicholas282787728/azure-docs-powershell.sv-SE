---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
ms.openlocfilehash: 4b3437f9df1be7e458aaa528769de406d755a071
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581188"
---
# <span data-ttu-id="9300e-101">Get-AzureRmHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="9300e-101">Get-AzureRmHDInsightProperties</span></span>

## <span data-ttu-id="9300e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9300e-102">SYNOPSIS</span></span>
<span data-ttu-id="9300e-103">Hämtar egenskaper för HDInsight-tjänsten, till exempel tillgängliga platser och kapacitet.</span><span class="sxs-lookup"><span data-stu-id="9300e-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9300e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9300e-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightProperties [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9300e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9300e-105">DESCRIPTION</span></span>
<span data-ttu-id="9300e-106">Cmdleten **Get-AzureRmHDInsightProperties** hämtar egenskaper som är specifika för Azure HDInsight, till exempel listan över tillgängliga platser, HDInsight-kluster versioner och tillgänglig beräknings kapacitet.</span><span class="sxs-lookup"><span data-stu-id="9300e-106">The **Get-AzureRmHDInsightProperties** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="9300e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9300e-107">EXAMPLES</span></span>

### <span data-ttu-id="9300e-108">Exempel 1: Hämta egenskaperna för ett Azure HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="9300e-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightProperties -Location "East US 2"
```

<span data-ttu-id="9300e-109">Det här kommandot får egenskaper från en HDInsight-tjänst från platsen östra USA 2.</span><span class="sxs-lookup"><span data-stu-id="9300e-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="9300e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9300e-110">PARAMETERS</span></span>

### <span data-ttu-id="9300e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9300e-111">-DefaultProfile</span></span>
<span data-ttu-id="9300e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9300e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9300e-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="9300e-113">-Location</span></span>
<span data-ttu-id="9300e-114">Anger platsen för vilken metabasegenskaper-egenskaper hämtas.</span><span class="sxs-lookup"><span data-stu-id="9300e-114">Specifies the location for which to fetch HDInsight properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9300e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9300e-115">CommonParameters</span></span>
<span data-ttu-id="9300e-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9300e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9300e-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9300e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9300e-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9300e-118">INPUTS</span></span>

### <span data-ttu-id="9300e-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="9300e-119">None</span></span>
<span data-ttu-id="9300e-120">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9300e-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9300e-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9300e-121">OUTPUTS</span></span>

### <span data-ttu-id="9300e-122">Microsoft. Azure. Management. HDInsight. Models. CapabilitiesResponse</span><span class="sxs-lookup"><span data-stu-id="9300e-122">Microsoft.Azure.Management.HDInsight.Models.CapabilitiesResponse</span></span>

## <span data-ttu-id="9300e-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9300e-123">NOTES</span></span>

## <span data-ttu-id="9300e-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9300e-124">RELATED LINKS</span></span>

