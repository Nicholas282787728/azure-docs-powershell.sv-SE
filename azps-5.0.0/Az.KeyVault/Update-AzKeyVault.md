---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 10a441cd1354b75a13b429c4375e7bc3fba72244
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263002"
---
# <span data-ttu-id="20dd8-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="20dd8-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="20dd8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20dd8-102">SYNOPSIS</span></span>
<span data-ttu-id="20dd8-103">Uppdatera tillståndet för ett Azure Key-valv.</span><span class="sxs-lookup"><span data-stu-id="20dd8-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="20dd8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20dd8-104">SYNTAX</span></span>

### <span data-ttu-id="20dd8-105">UpdateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="20dd8-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20dd8-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20dd8-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20dd8-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20dd8-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20dd8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20dd8-108">DESCRIPTION</span></span>
<span data-ttu-id="20dd8-109">Denna cmdlet uppdaterar tillståndet för ett Azure Key-valv.</span><span class="sxs-lookup"><span data-stu-id="20dd8-109">This cmdlet updates the state of an Azure key vault.</span></span>

## <span data-ttu-id="20dd8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20dd8-110">EXAMPLES</span></span>

### <span data-ttu-id="20dd8-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="20dd8-111">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="20dd8-112">Aktiverar rensa skydd med rör-syntax.</span><span class="sxs-lookup"><span data-stu-id="20dd8-112">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="20dd8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20dd8-113">PARAMETERS</span></span>

### <span data-ttu-id="20dd8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20dd8-114">-DefaultProfile</span></span>
<span data-ttu-id="20dd8-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20dd8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20dd8-116">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="20dd8-116">-EnablePurgeProtection</span></span>
<span data-ttu-id="20dd8-117">Aktivera funktionerna för rensnings skydd för det här nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="20dd8-117">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="20dd8-118">När den är aktive rad kan den inte avaktiveras.</span><span class="sxs-lookup"><span data-stu-id="20dd8-118">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="20dd8-119">Borttagning krävs för att den ska vara aktive rad.</span><span class="sxs-lookup"><span data-stu-id="20dd8-119">It requires soft-delete to be turned on.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20dd8-120">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="20dd8-120">-EnableRbacAuthorization</span></span>
<span data-ttu-id="20dd8-121">Aktivera eller inaktivera det här nyckelvärdet för att tillåta data åtgärder via RBAC (rollbaserad åtkomst kontroll).</span><span class="sxs-lookup"><span data-stu-id="20dd8-121">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20dd8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20dd8-122">-InputObject</span></span>
<span data-ttu-id="20dd8-123">Key valv-objekt.</span><span class="sxs-lookup"><span data-stu-id="20dd8-123">Key vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20dd8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20dd8-124">-ResourceGroupName</span></span>
<span data-ttu-id="20dd8-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="20dd8-125">Name of the resource group.</span></span>

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

### <span data-ttu-id="20dd8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20dd8-126">-ResourceId</span></span>
<span data-ttu-id="20dd8-127">Resurs-ID för huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="20dd8-127">Resource ID of the key vault.</span></span>

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

### <span data-ttu-id="20dd8-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="20dd8-128">-VaultName</span></span>
<span data-ttu-id="20dd8-129">Namn på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="20dd8-129">Name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20dd8-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="20dd8-130">-Confirm</span></span>
<span data-ttu-id="20dd8-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="20dd8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20dd8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20dd8-132">-WhatIf</span></span>
<span data-ttu-id="20dd8-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="20dd8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20dd8-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="20dd8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20dd8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20dd8-135">CommonParameters</span></span>
<span data-ttu-id="20dd8-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20dd8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20dd8-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20dd8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20dd8-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20dd8-138">INPUTS</span></span>

### <span data-ttu-id="20dd8-139">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="20dd8-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="20dd8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="20dd8-140">System.String</span></span>

## <span data-ttu-id="20dd8-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20dd8-141">OUTPUTS</span></span>

### <span data-ttu-id="20dd8-142">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="20dd8-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="20dd8-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20dd8-143">NOTES</span></span>

## <span data-ttu-id="20dd8-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20dd8-144">RELATED LINKS</span></span>
