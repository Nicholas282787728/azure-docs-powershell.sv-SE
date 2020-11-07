---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: c7d357df084a3843f8accbd3f54cc8aba9085012
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744095"
---
# <span data-ttu-id="17218-101">Enable-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="17218-101">Enable-AzHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="17218-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17218-102">SYNOPSIS</span></span>
<span data-ttu-id="17218-103">Aktiverar Operations Management Suite (OMS) i ett HDInsight-kluster och relevanta loggar skickas till den OMS-arbetsyta som anges vid aktivering.</span><span class="sxs-lookup"><span data-stu-id="17218-103">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

## <span data-ttu-id="17218-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17218-104">SYNTAX</span></span>

```
Enable-AzHDInsightOperationsManagementSuite [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17218-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17218-105">DESCRIPTION</span></span>
<span data-ttu-id="17218-106">Cmdleten **Enable-AzHDInsightOperationsManagementSuite** aktiverar Operations Management Suite (OMS) i ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="17218-106">The **Enable-AzHDInsightOperationsManagementSuite** cmdlet enables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="17218-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17218-107">EXAMPLES</span></span>

### <span data-ttu-id="17218-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="17218-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightOMS -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="17218-109">Operations Management Suite (OMS) aktive ras i HDInsight-klustret och relevanta loggar skickas till OMS-arbetsytan med ID 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="17218-109">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="17218-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="17218-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="17218-111">Operations Management Suite (OMS) aktive ras i HDInsight-klustret och relevanta loggar skickas till OMS-arbetsytan med ID 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="17218-111">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="17218-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17218-112">PARAMETERS</span></span>

### <span data-ttu-id="17218-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17218-113">-DefaultProfile</span></span>
<span data-ttu-id="17218-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="17218-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17218-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="17218-115">-Name</span></span>
<span data-ttu-id="17218-116">Namnet på klustret för att aktivera Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="17218-116">The name of the cluster to enable Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="17218-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="17218-117">-PrimaryKey</span></span>
<span data-ttu-id="17218-118">Primärt för arbets ytan Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="17218-118">The primary key of the Operations Management Suite(OMS) workspace.</span></span>

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

### <span data-ttu-id="17218-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17218-119">-ResourceGroupName</span></span>
<span data-ttu-id="17218-120">Klustrets resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="17218-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="17218-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="17218-121">-WorkspaceId</span></span>
<span data-ttu-id="17218-122">ID för arbets ytan Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="17218-122">The id of the Operations Management Suite(OMS) workspace.</span></span>

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

### <span data-ttu-id="17218-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="17218-123">-Confirm</span></span>
<span data-ttu-id="17218-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="17218-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17218-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17218-125">-WhatIf</span></span>
<span data-ttu-id="17218-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="17218-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17218-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="17218-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17218-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17218-128">CommonParameters</span></span>
<span data-ttu-id="17218-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17218-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17218-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17218-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17218-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17218-131">INPUTS</span></span>

### <span data-ttu-id="17218-132">System. String</span><span class="sxs-lookup"><span data-stu-id="17218-132">System.String</span></span>

## <span data-ttu-id="17218-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17218-133">OUTPUTS</span></span>

### <span data-ttu-id="17218-134">Microsoft. Azure. Management. HDInsight. Models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="17218-134">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="17218-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17218-135">NOTES</span></span>

## <span data-ttu-id="17218-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17218-136">RELATED LINKS</span></span>
