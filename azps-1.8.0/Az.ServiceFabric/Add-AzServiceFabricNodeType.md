---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
ms.openlocfilehash: 2c489a0d041e982b6a870102db73268b7abe5392
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746845"
---
# <span data-ttu-id="81119-101">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="81119-101">Add-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="81119-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="81119-102">SYNOPSIS</span></span>
<span data-ttu-id="81119-103">Lägg till en ny nodtyp i det befintliga klustret.</span><span class="sxs-lookup"><span data-stu-id="81119-103">Add a new node type to the existing cluster.</span></span>

## <span data-ttu-id="81119-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="81119-104">SYNTAX</span></span>

```
Add-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81119-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="81119-105">DESCRIPTION</span></span>
<span data-ttu-id="81119-106">Lägga till en ny nodtyp i ett befintligt kluster.</span><span class="sxs-lookup"><span data-stu-id="81119-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="81119-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="81119-107">EXAMPLES</span></span>

### <span data-ttu-id="81119-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="81119-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="81119-109">Det här kommandot lägger till en ny NodeType ' N2 ' med kapaciteten 5 och namnet på den virtuella dator administratören är ' adminName '.</span><span class="sxs-lookup"><span data-stu-id="81119-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="81119-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="81119-110">PARAMETERS</span></span>

### <span data-ttu-id="81119-111">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="81119-111">-Capacity</span></span>
<span data-ttu-id="81119-112">Volymen</span><span class="sxs-lookup"><span data-stu-id="81119-112">Capacity</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81119-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81119-113">-DefaultProfile</span></span>
<span data-ttu-id="81119-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="81119-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81119-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="81119-115">-DurabilityLevel</span></span>
<span data-ttu-id="81119-116">Ange livs längden för NodeType.</span><span class="sxs-lookup"><span data-stu-id="81119-116">Specify the durability level of the NodeType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases:
Accepted values: Bronze, Silver, Gold

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81119-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="81119-117">-Name</span></span>
<span data-ttu-id="81119-118">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="81119-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81119-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="81119-119">-NodeType</span></span>
<span data-ttu-id="81119-120">Namnet på nodtypen.</span><span class="sxs-lookup"><span data-stu-id="81119-120">The node type name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81119-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81119-121">-ResourceGroupName</span></span>
<span data-ttu-id="81119-122">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="81119-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="81119-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="81119-123">-Tier</span></span>
<span data-ttu-id="81119-124">SKU-nivå för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="81119-124">Vm Sku Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81119-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="81119-125">-VmPassword</span></span>
<span data-ttu-id="81119-126">Lösen ordet för inloggning till den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="81119-126">The password of login to the Vm.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81119-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="81119-127">-VmSku</span></span>
<span data-ttu-id="81119-128">SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="81119-128">The sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81119-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="81119-129">-VmUserName</span></span>
<span data-ttu-id="81119-130">Användar namnet för inloggning till VM.</span><span class="sxs-lookup"><span data-stu-id="81119-130">The user name for login to Vm.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81119-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="81119-131">-Confirm</span></span>
<span data-ttu-id="81119-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="81119-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81119-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81119-133">-WhatIf</span></span>
<span data-ttu-id="81119-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="81119-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81119-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="81119-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81119-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81119-136">CommonParameters</span></span>
<span data-ttu-id="81119-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81119-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81119-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81119-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81119-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="81119-139">INPUTS</span></span>

### <span data-ttu-id="81119-140">System. String</span><span class="sxs-lookup"><span data-stu-id="81119-140">System.String</span></span>

### <span data-ttu-id="81119-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="81119-141">System.Int32</span></span>

### <span data-ttu-id="81119-142">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="81119-142">System.Security.SecureString</span></span>

### <span data-ttu-id="81119-143">Microsoft. Azure. commands. ServiceFabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="81119-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="81119-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="81119-144">OUTPUTS</span></span>

### <span data-ttu-id="81119-145">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="81119-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="81119-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="81119-146">NOTES</span></span>

## <span data-ttu-id="81119-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="81119-147">RELATED LINKS</span></span>