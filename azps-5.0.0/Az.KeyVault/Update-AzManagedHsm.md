---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsm.md
ms.openlocfilehash: 49e8e5aeddba1b15c97155a200413ea774c8a7a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273417"
---
# <span data-ttu-id="669b9-101">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="669b9-101">Update-AzManagedHsm</span></span>

## <span data-ttu-id="669b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="669b9-102">SYNOPSIS</span></span>
<span data-ttu-id="669b9-103">Uppdatera statusen för en Azure Managed HSM.</span><span class="sxs-lookup"><span data-stu-id="669b9-103">Update the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="669b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="669b9-104">SYNTAX</span></span>

### <span data-ttu-id="669b9-105">UpdateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="669b9-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzManagedHsm -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="669b9-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="669b9-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzManagedHsm -InputObject <PSManagedHsm> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="669b9-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="669b9-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzManagedHsm -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="669b9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="669b9-108">DESCRIPTION</span></span>
<span data-ttu-id="669b9-109">Denna cmdlet uppdaterar tillståndet för en Azure Managed HSM.</span><span class="sxs-lookup"><span data-stu-id="669b9-109">This cmdlet updates the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="669b9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="669b9-110">EXAMPLES</span></span>

### <span data-ttu-id="669b9-111">Exempel 1: uppdatera en hanterad HSM direkt</span><span class="sxs-lookup"><span data-stu-id="669b9-111">Example 1: Update a managed Hsm directly</span></span>
```powershell
PS C:\> Update-AzManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName -Tag @{testKey="testValue"} | fl

Managed HSM Name                    : testmhsm
Resource Group Name                 : testmhsm
Location                            : eastus2euap
Resource ID                         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testmhsm/provid
                                      ers/Microsoft.KeyVault/managedHSMs/testmhsm
HSM Pool URI                        :
Tenant ID                           : xxxxxx-xxxx-xxxx-xxxxxxxxxxxx
Initial Admin Object Ids            : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SKU                                 : StandardB1
Soft Delete Enabled?                : True
Enabled Purge Protection?           : False
Soft Delete Retention Period (days) : 90
Provisioning State                  : Provisioning
Status Message                      : Resource creation in progress. Starting service...
Tags                                :
                                      Name        Value
                                      ====        =====
                                      testKey     testValued
```

<span data-ttu-id="669b9-112">Uppdaterar taggar för den hanterade HSM som heter `$hsmName` i resurs gruppen `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="669b9-112">Updates tags for the managed Hsm named `$hsmName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="669b9-113">Exempel 2: uppdatera en hanterad HSM med hjälp av</span><span class="sxs-lookup"><span data-stu-id="669b9-113">Example 2: Update a managed Hsm using piping</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName | Update-AzManagedHsm -Tag @{testKey="testValue"}
```

<span data-ttu-id="669b9-114">Uppdaterar taggar för hanterad HSM med rör-syntax.</span><span class="sxs-lookup"><span data-stu-id="669b9-114">Updates tags for the managed Hsm using piping syntax.</span></span>

## <span data-ttu-id="669b9-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="669b9-115">PARAMETERS</span></span>

### <span data-ttu-id="669b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="669b9-116">-DefaultProfile</span></span>
<span data-ttu-id="669b9-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="669b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="669b9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="669b9-118">-InputObject</span></span>
<span data-ttu-id="669b9-119">Hanterat HSM-objekt.</span><span class="sxs-lookup"><span data-stu-id="669b9-119">Managed HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="669b9-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="669b9-120">-Name</span></span>
<span data-ttu-id="669b9-121">Namnet på den hanterade HSM.</span><span class="sxs-lookup"><span data-stu-id="669b9-121">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="669b9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="669b9-122">-ResourceGroupName</span></span>
<span data-ttu-id="669b9-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="669b9-123">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="669b9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="669b9-124">-ResourceId</span></span>
<span data-ttu-id="669b9-125">Resurs-ID för hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="669b9-125">Resource ID of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="669b9-126">-Tagg</span><span class="sxs-lookup"><span data-stu-id="669b9-126">-Tag</span></span>
<span data-ttu-id="669b9-127">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="669b9-127">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="669b9-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="669b9-128">-Confirm</span></span>
<span data-ttu-id="669b9-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="669b9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="669b9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="669b9-130">-WhatIf</span></span>
<span data-ttu-id="669b9-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="669b9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="669b9-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="669b9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="669b9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="669b9-133">CommonParameters</span></span>
<span data-ttu-id="669b9-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="669b9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="669b9-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="669b9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="669b9-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="669b9-136">INPUTS</span></span>

### <span data-ttu-id="669b9-137">Microsoft. Azure. commands. valv. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="669b9-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="669b9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="669b9-138">System.String</span></span>

### <span data-ttu-id="669b9-139">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="669b9-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="669b9-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="669b9-140">OUTPUTS</span></span>

### <span data-ttu-id="669b9-141">Microsoft. Azure. commands. valv. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="669b9-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="669b9-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="669b9-142">NOTES</span></span>

## <span data-ttu-id="669b9-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="669b9-143">RELATED LINKS</span></span>

[<span data-ttu-id="669b9-144">New-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="669b9-144">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="669b9-145">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="669b9-145">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="669b9-146">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="669b9-146">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)