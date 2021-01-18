---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: 690b00c41aea571786916d2055eb4063c51c4370
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525421"
---
# <span data-ttu-id="1aaf0-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="1aaf0-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="1aaf0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1aaf0-102">SYNOPSIS</span></span>
<span data-ttu-id="1aaf0-103">Skapa en ny program typ för tjänst Fabric under den angivna resurs gruppen och klustret.</span><span class="sxs-lookup"><span data-stu-id="1aaf0-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="1aaf0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1aaf0-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aaf0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1aaf0-105">DESCRIPTION</span></span>
<span data-ttu-id="1aaf0-106">Cmdleten skapar en ny typ av tjänst infrastruktur program under den angivna resurs gruppen och klustret.</span><span class="sxs-lookup"><span data-stu-id="1aaf0-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="1aaf0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1aaf0-107">EXAMPLES</span></span>

### <span data-ttu-id="1aaf0-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1aaf0-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="1aaf0-109">I det här exemplet skapas ett nytt program med "testAppType" under den resurs grupp och det kluster som anges.</span><span class="sxs-lookup"><span data-stu-id="1aaf0-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="1aaf0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1aaf0-110">PARAMETERS</span></span>

### <span data-ttu-id="1aaf0-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="1aaf0-111">-ClusterName</span></span>
<span data-ttu-id="1aaf0-112">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="1aaf0-112">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1aaf0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aaf0-113">-DefaultProfile</span></span>
<span data-ttu-id="1aaf0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1aaf0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1aaf0-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="1aaf0-115">-Name</span></span>
<span data-ttu-id="1aaf0-116">Ange namnet på program typen</span><span class="sxs-lookup"><span data-stu-id="1aaf0-116">Specify the name of the application type</span></span>

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

### <span data-ttu-id="1aaf0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aaf0-117">-ResourceGroupName</span></span>
<span data-ttu-id="1aaf0-118">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1aaf0-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1aaf0-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1aaf0-119">-Confirm</span></span>
<span data-ttu-id="1aaf0-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1aaf0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aaf0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aaf0-121">-WhatIf</span></span>
<span data-ttu-id="1aaf0-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1aaf0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1aaf0-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1aaf0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1aaf0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aaf0-124">CommonParameters</span></span>
<span data-ttu-id="1aaf0-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aaf0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aaf0-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1aaf0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aaf0-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1aaf0-127">INPUTS</span></span>

### <span data-ttu-id="1aaf0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1aaf0-128">System.String</span></span>

## <span data-ttu-id="1aaf0-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1aaf0-129">OUTPUTS</span></span>

### <span data-ttu-id="1aaf0-130">Microsoft. Azure. commands. ServiceFabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="1aaf0-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="1aaf0-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1aaf0-131">NOTES</span></span>

## <span data-ttu-id="1aaf0-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1aaf0-132">RELATED LINKS</span></span>
