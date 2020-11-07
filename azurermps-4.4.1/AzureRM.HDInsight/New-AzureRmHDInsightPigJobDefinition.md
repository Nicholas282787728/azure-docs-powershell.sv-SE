---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightPigJobDefinition.md
ms.openlocfilehash: 7045131d7f94aab65ec1947f9fe65d25347c9f97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758071"
---
# <span data-ttu-id="252ef-101">New-AzureRmHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="252ef-101">New-AzureRmHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="252ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="252ef-102">SYNOPSIS</span></span>
<span data-ttu-id="252ef-103">Skapar ett gris-Job-objekt.</span><span class="sxs-lookup"><span data-stu-id="252ef-103">Creates a Pig job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="252ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="252ef-104">SYNTAX</span></span>

```
New-AzureRmHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="252ef-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="252ef-105">DESCRIPTION</span></span>
<span data-ttu-id="252ef-106">Cmdleten **New-AzureRmHDInsightPigJobDefinition** definierar ett gris-jobb-objekt som ska användas med ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="252ef-106">The **New-AzureRmHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="252ef-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="252ef-107">EXAMPLES</span></span>

### <span data-ttu-id="252ef-108">Exempel 1: skapa en jobb definition för gris</span><span class="sxs-lookup"><span data-stu-id="252ef-108">Example 1: Create a Pig job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Pig job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightPigJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="252ef-109">Det här kommandot skapar en jobb definition för gris.</span><span class="sxs-lookup"><span data-stu-id="252ef-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="252ef-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="252ef-110">PARAMETERS</span></span>

### <span data-ttu-id="252ef-111">-Argument</span><span class="sxs-lookup"><span data-stu-id="252ef-111">-Arguments</span></span>
<span data-ttu-id="252ef-112">Anger en matris med argument för jobbet.</span><span class="sxs-lookup"><span data-stu-id="252ef-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="252ef-113">Argumenten skickas som kommando rads argument till varje aktivitet.</span><span class="sxs-lookup"><span data-stu-id="252ef-113">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252ef-114">-Fil</span><span class="sxs-lookup"><span data-stu-id="252ef-114">-File</span></span>
<span data-ttu-id="252ef-115">Anger sökvägen till en fil som innehåller den fråga som ska köras.</span><span class="sxs-lookup"><span data-stu-id="252ef-115">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="252ef-116">Filen måste finnas tillgänglig på det lagrings konto som är kopplat till klustret.</span><span class="sxs-lookup"><span data-stu-id="252ef-116">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="252ef-117">Du kan använda den här parametern i stället för *Frågeparametern* .</span><span class="sxs-lookup"><span data-stu-id="252ef-117">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252ef-118">-Filer</span><span class="sxs-lookup"><span data-stu-id="252ef-118">-Files</span></span>
<span data-ttu-id="252ef-119">Anger en samling filer som associeras med ett struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="252ef-119">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252ef-120">-Fråga</span><span class="sxs-lookup"><span data-stu-id="252ef-120">-Query</span></span>
<span data-ttu-id="252ef-121">Anger gris-frågan.</span><span class="sxs-lookup"><span data-stu-id="252ef-121">Specifies the Pig query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252ef-122">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="252ef-122">-StatusFolder</span></span>
<span data-ttu-id="252ef-123">Anger platsen för mappen som innehåller standardutdata och fel utdata för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="252ef-123">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252ef-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="252ef-124">-DefaultProfile</span></span>
<span data-ttu-id="252ef-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="252ef-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="252ef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="252ef-126">CommonParameters</span></span>
<span data-ttu-id="252ef-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="252ef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="252ef-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="252ef-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="252ef-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="252ef-129">INPUTS</span></span>

## <span data-ttu-id="252ef-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="252ef-130">OUTPUTS</span></span>

### <span data-ttu-id="252ef-131">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="252ef-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="252ef-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="252ef-132">NOTES</span></span>

## <span data-ttu-id="252ef-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="252ef-133">RELATED LINKS</span></span>

[<span data-ttu-id="252ef-134">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="252ef-134">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


