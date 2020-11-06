---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 0bae150e60332e4f1bb0ee4f2ee67699c13eb5e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574174"
---
# <span data-ttu-id="eb301-101">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="eb301-101">Add-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="eb301-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb301-102">SYNOPSIS</span></span>
<span data-ttu-id="eb301-103">Lägg till en ny nodtyp i det befintliga klustret.</span><span class="sxs-lookup"><span data-stu-id="eb301-103">Add a new node type to the existing cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb301-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb301-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb301-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb301-105">DESCRIPTION</span></span>
<span data-ttu-id="eb301-106">Lägga till en ny nodtyp i ett befintligt kluster.</span><span class="sxs-lookup"><span data-stu-id="eb301-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="eb301-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb301-107">EXAMPLES</span></span>

### <span data-ttu-id="eb301-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eb301-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="eb301-109">Det här kommandot lägger till en ny NodeType ' N2 ' med kapaciteten 5 och namnet på den virtuella dator administratören är ' adminName '.</span><span class="sxs-lookup"><span data-stu-id="eb301-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="eb301-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb301-110">PARAMETERS</span></span>

### <span data-ttu-id="eb301-111">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="eb301-111">-Capacity</span></span>
<span data-ttu-id="eb301-112">Volymen</span><span class="sxs-lookup"><span data-stu-id="eb301-112">Capacity</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb301-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb301-113">-DefaultProfile</span></span>
<span data-ttu-id="eb301-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eb301-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb301-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="eb301-115">-DurabilityLevel</span></span>
<span data-ttu-id="eb301-116">Ange livs längden för NodeType.</span><span class="sxs-lookup"><span data-stu-id="eb301-116">Specify the durability level of the NodeType.</span></span>

```yaml
Type: DurabilityLevel
Parameter Sets: (All)
Aliases: 
Accepted values: Bronze, Silver, Gold

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb301-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb301-117">-Name</span></span>
<span data-ttu-id="eb301-118">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="eb301-118">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb301-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="eb301-119">-NodeType</span></span>
<span data-ttu-id="eb301-120">Namnet på nodtypen.</span><span class="sxs-lookup"><span data-stu-id="eb301-120">The node type name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb301-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb301-121">-ResourceGroupName</span></span>
<span data-ttu-id="eb301-122">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="eb301-122">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb301-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="eb301-123">-Tier</span></span>
<span data-ttu-id="eb301-124">SKU-nivå för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="eb301-124">Vm Sku Tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb301-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="eb301-125">-VmPassword</span></span>
<span data-ttu-id="eb301-126">Lösen ordet för inloggning till den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="eb301-126">The password of login to the Vm.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb301-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="eb301-127">-VmSku</span></span>
<span data-ttu-id="eb301-128">SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="eb301-128">The sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb301-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="eb301-129">-VmUserName</span></span>
<span data-ttu-id="eb301-130">Användar namnet för inloggning till VM.</span><span class="sxs-lookup"><span data-stu-id="eb301-130">The user name for login to Vm.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb301-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eb301-131">-Confirm</span></span>
<span data-ttu-id="eb301-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eb301-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb301-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb301-133">-WhatIf</span></span>
<span data-ttu-id="eb301-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eb301-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb301-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eb301-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb301-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb301-136">CommonParameters</span></span>
<span data-ttu-id="eb301-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb301-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb301-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb301-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb301-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb301-139">INPUTS</span></span>

### <span data-ttu-id="eb301-140">System. String</span><span class="sxs-lookup"><span data-stu-id="eb301-140">System.String</span></span>
<span data-ttu-id="eb301-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="eb301-141">System.Int32</span></span>

## <span data-ttu-id="eb301-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb301-142">OUTPUTS</span></span>

### <span data-ttu-id="eb301-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="eb301-143">System.Object</span></span>

## <span data-ttu-id="eb301-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb301-144">NOTES</span></span>

## <span data-ttu-id="eb301-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb301-145">RELATED LINKS</span></span>

