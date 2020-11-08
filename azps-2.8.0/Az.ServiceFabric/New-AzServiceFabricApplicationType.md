---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: 983edfae4876e2998d4134a679e76b64751ef0d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919928"
---
# <span data-ttu-id="eab61-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="eab61-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="eab61-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eab61-102">SYNOPSIS</span></span>
<span data-ttu-id="eab61-103">Skapa en ny program typ för tjänst Fabric under den angivna resurs gruppen och klustret.</span><span class="sxs-lookup"><span data-stu-id="eab61-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="eab61-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eab61-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eab61-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eab61-105">DESCRIPTION</span></span>
<span data-ttu-id="eab61-106">Cmdleten skapar en ny typ av tjänst infrastruktur program under den angivna resurs gruppen och klustret.</span><span class="sxs-lookup"><span data-stu-id="eab61-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="eab61-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eab61-107">EXAMPLES</span></span>

### <span data-ttu-id="eab61-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eab61-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="eab61-109">I det här exemplet skapas ett nytt program med "testAppType" under den resurs grupp och det kluster som anges.</span><span class="sxs-lookup"><span data-stu-id="eab61-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="eab61-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eab61-110">PARAMETERS</span></span>

### <span data-ttu-id="eab61-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="eab61-111">-ClusterName</span></span>
<span data-ttu-id="eab61-112">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="eab61-112">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="eab61-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eab61-113">-DefaultProfile</span></span>
<span data-ttu-id="eab61-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eab61-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eab61-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="eab61-115">-Name</span></span>
<span data-ttu-id="eab61-116">Ange namnet på program typen</span><span class="sxs-lookup"><span data-stu-id="eab61-116">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eab61-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eab61-117">-ResourceGroupName</span></span>
<span data-ttu-id="eab61-118">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="eab61-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="eab61-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eab61-119">-Confirm</span></span>
<span data-ttu-id="eab61-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eab61-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eab61-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eab61-121">-WhatIf</span></span>
<span data-ttu-id="eab61-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eab61-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eab61-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eab61-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eab61-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eab61-124">CommonParameters</span></span>
<span data-ttu-id="eab61-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eab61-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eab61-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eab61-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eab61-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eab61-127">INPUTS</span></span>

### <span data-ttu-id="eab61-128">System. String</span><span class="sxs-lookup"><span data-stu-id="eab61-128">System.String</span></span>

## <span data-ttu-id="eab61-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eab61-129">OUTPUTS</span></span>

### <span data-ttu-id="eab61-130">Microsoft. Azure. commands. ServiceFabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="eab61-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="eab61-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eab61-131">NOTES</span></span>

## <span data-ttu-id="eab61-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eab61-132">RELATED LINKS</span></span>