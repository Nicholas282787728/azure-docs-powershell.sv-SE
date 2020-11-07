---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/enable-azurermhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Enable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Enable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 3ea06c98119775616cd8d5a4dbb8788dba4380bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755839"
---
# <span data-ttu-id="a0810-101">Enable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="a0810-101">Enable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="a0810-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0810-102">SYNOPSIS</span></span>
<span data-ttu-id="a0810-103">Aktiverar Operations Management Suite (OMS) i ett HDInsight-kluster och relevanta loggar skickas till den OMS-arbetsyta som anges vid aktivering.</span><span class="sxs-lookup"><span data-stu-id="a0810-103">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0810-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0810-104">SYNTAX</span></span>

```
Enable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-WorkspaceId] <String>
 [-PrimaryKey] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0810-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0810-105">DESCRIPTION</span></span>
<span data-ttu-id="a0810-106">Cmdleten **Enable-AzureRmHDInsightOperationsManagementSuite** aktiverar Operations Management Suite (OMS) i ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="a0810-106">The **Enable-AzureRmHDInsightOperationsManagementSuite** cmdlet enables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="a0810-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0810-107">EXAMPLES</span></span>

### <span data-ttu-id="a0810-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a0810-108">Example 1</span></span>
```
PS C:\> Enable-AzureRmHDInsightOMS -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="a0810-109">Operations Management Suite (OMS) aktive ras i HDInsight-klustret och relevanta loggar skickas till OMS-arbetsytan med ID 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="a0810-109">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="a0810-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a0810-110">Example 2</span></span>
```
PS C:\> Enable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="a0810-111">Operations Management Suite (OMS) aktive ras i HDInsight-klustret och relevanta loggar skickas till OMS-arbetsytan med ID 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="a0810-111">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="a0810-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0810-112">PARAMETERS</span></span>

### <span data-ttu-id="a0810-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0810-113">-DefaultProfile</span></span>
<span data-ttu-id="a0810-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a0810-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0810-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="a0810-115">-Name</span></span>
<span data-ttu-id="a0810-116">Namnet på klustret för att aktivera Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="a0810-116">The name of the cluster to enable Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="a0810-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="a0810-117">-PrimaryKey</span></span>
<span data-ttu-id="a0810-118">Primärt för arbets ytan Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="a0810-118">The primary key of the Operations Management Suite(OMS) workspace.</span></span>

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

### <span data-ttu-id="a0810-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0810-119">-ResourceGroupName</span></span>
<span data-ttu-id="a0810-120">Klustrets resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a0810-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="a0810-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="a0810-121">-WorkspaceId</span></span>
<span data-ttu-id="a0810-122">ID för arbets ytan Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="a0810-122">The id of the Operations Management Suite(OMS) workspace.</span></span>

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

### <span data-ttu-id="a0810-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a0810-123">-Confirm</span></span>
<span data-ttu-id="a0810-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a0810-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0810-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0810-125">-WhatIf</span></span>
<span data-ttu-id="a0810-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a0810-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0810-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a0810-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0810-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0810-128">CommonParameters</span></span>
<span data-ttu-id="a0810-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0810-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0810-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0810-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0810-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0810-131">INPUTS</span></span>

### <span data-ttu-id="a0810-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a0810-132">System.String</span></span>

## <span data-ttu-id="a0810-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0810-133">OUTPUTS</span></span>

### <span data-ttu-id="a0810-134">Microsoft. Azure. Management. HDInsight. Models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="a0810-134">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="a0810-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0810-135">NOTES</span></span>

## <span data-ttu-id="a0810-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0810-136">RELATED LINKS</span></span>
