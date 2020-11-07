---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Enable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Enable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: fcaa5c1342801c4c0ef00e1a4c48abf4a6b4da41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756348"
---
# <span data-ttu-id="7870e-101">Enable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="7870e-101">Enable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="7870e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7870e-102">SYNOPSIS</span></span>
<span data-ttu-id="7870e-103">Aktiverar Operations Management Suite (OMS) i ett HDInsight-kluster och relevanta loggar skickas till den OMS-arbetsyta som anges vid aktivering.</span><span class="sxs-lookup"><span data-stu-id="7870e-103">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7870e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7870e-104">SYNTAX</span></span>

```
Enable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-WorkspaceId] <String>
 [-PrimaryKey] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7870e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7870e-105">DESCRIPTION</span></span>
<span data-ttu-id="7870e-106">Cmdleten **Enable-AzureRmHDInsightOperationsManagementSuite** aktiverar Operations Management Suite (OMS) i ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="7870e-106">The **Enable-AzureRmHDInsightOperationsManagementSuite** cmdlet enables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="7870e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7870e-107">EXAMPLES</span></span>

### <span data-ttu-id="7870e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7870e-108">Example 1</span></span>
```
PS C:\> Enable-AzureRmHDInsightOMS -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="7870e-109">Operations Management Suite (OMS) aktive ras i HDInsight-klustret och relevanta loggar skickas till OMS-arbetsytan med ID 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="7870e-109">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="7870e-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7870e-110">Example 2</span></span>
```
PS C:\> Enable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="7870e-111">Operations Management Suite (OMS) aktive ras i HDInsight-klustret och relevanta loggar skickas till OMS-arbetsytan med ID 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="7870e-111">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="7870e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7870e-112">PARAMETERS</span></span>

### <span data-ttu-id="7870e-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="7870e-113">-Name</span></span>
<span data-ttu-id="7870e-114">Namnet på klustret för att aktivera Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="7870e-114">The name of the cluster to enable Operations Management Suite(OMS).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7870e-115">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="7870e-115">-PrimaryKey</span></span>
<span data-ttu-id="7870e-116">Primärt för arbets ytan Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="7870e-116">The primary key of the Operations Management Suite(OMS) workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7870e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7870e-117">-ResourceGroupName</span></span>
<span data-ttu-id="7870e-118">Klustrets resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="7870e-118">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7870e-119">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="7870e-119">-WorkspaceId</span></span>
<span data-ttu-id="7870e-120">ID för arbets ytan Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="7870e-120">The id of the Operations Management Suite(OMS) workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7870e-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7870e-121">-Confirm</span></span>
<span data-ttu-id="7870e-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7870e-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7870e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7870e-123">-DefaultProfile</span></span>
<span data-ttu-id="7870e-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7870e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7870e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7870e-125">-WhatIf</span></span>
<span data-ttu-id="7870e-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7870e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7870e-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7870e-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7870e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7870e-128">CommonParameters</span></span>
<span data-ttu-id="7870e-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7870e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7870e-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7870e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7870e-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7870e-131">INPUTS</span></span>

### <span data-ttu-id="7870e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7870e-132">System.String</span></span>

## <span data-ttu-id="7870e-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7870e-133">OUTPUTS</span></span>

### <span data-ttu-id="7870e-134">Microsoft. Azure. Management. HDInsight. Models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="7870e-134">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="7870e-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7870e-135">NOTES</span></span>

## <span data-ttu-id="7870e-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7870e-136">RELATED LINKS</span></span>

