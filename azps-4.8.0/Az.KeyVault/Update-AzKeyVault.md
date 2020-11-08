---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 4302f2f9c4c2d6b2c7afa879fc28e2ff4edbb592
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259427"
---
# <span data-ttu-id="07f9d-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="07f9d-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="07f9d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="07f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="07f9d-103">Uppdatera tillståndet för ett Azure Key-valv.</span><span class="sxs-lookup"><span data-stu-id="07f9d-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="07f9d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="07f9d-104">SYNTAX</span></span>

### <span data-ttu-id="07f9d-105">UpdateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="07f9d-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07f9d-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07f9d-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07f9d-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07f9d-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07f9d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="07f9d-108">DESCRIPTION</span></span>
<span data-ttu-id="07f9d-109">Denna cmdlet uppdaterar tillståndet för ett Azure Key-valv.</span><span class="sxs-lookup"><span data-stu-id="07f9d-109">This cmdlet updates the state of an Azure key vault.</span></span>
<span data-ttu-id="07f9d-110">Observera att om du uppdaterar vissa egenskaper är en irreversibl åtgärd, till exempel när en mjuk borttagning har Aktiver ATS kan den inte inaktive ras längre.</span><span class="sxs-lookup"><span data-stu-id="07f9d-110">Please note updating some of the properties is an irreversible action, for example once soft delete has been enabled, it cannot be disabled anymore.</span></span>

## <span data-ttu-id="07f9d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="07f9d-111">EXAMPLES</span></span>

### <span data-ttu-id="07f9d-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="07f9d-112">Example 1</span></span>
```powershell
PS C:\> Update-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName -EnableSoftDelete
```

<span data-ttu-id="07f9d-113">Aktiverar mjuk borttagning på Key Vault som heter `$keyVaultName` i resurs gruppen `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="07f9d-113">Enables soft delete on the key vault named `$keyVaultName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="07f9d-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="07f9d-114">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="07f9d-115">Aktiverar rensa skydd med rör-syntax.</span><span class="sxs-lookup"><span data-stu-id="07f9d-115">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="07f9d-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="07f9d-116">PARAMETERS</span></span>

### <span data-ttu-id="07f9d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f9d-117">-DefaultProfile</span></span>
<span data-ttu-id="07f9d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="07f9d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07f9d-119">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="07f9d-119">-EnablePurgeProtection</span></span>
<span data-ttu-id="07f9d-120">Aktivera funktionerna för rensnings skydd för det här nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="07f9d-120">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="07f9d-121">När den är aktive rad kan den inte avaktiveras.</span><span class="sxs-lookup"><span data-stu-id="07f9d-121">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="07f9d-122">Borttagning krävs för att den ska vara aktive rad.</span><span class="sxs-lookup"><span data-stu-id="07f9d-122">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="07f9d-123">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="07f9d-123">-EnableRbacAuthorization</span></span>
<span data-ttu-id="07f9d-124">Aktivera eller inaktivera det här nyckelvärdet för att tillåta data åtgärder via RBAC (rollbaserad åtkomst kontroll).</span><span class="sxs-lookup"><span data-stu-id="07f9d-124">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

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

### <span data-ttu-id="07f9d-125">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="07f9d-125">-EnableSoftDelete</span></span>
<span data-ttu-id="07f9d-126">Aktivera funktionerna för mjuk borttagning för det här nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="07f9d-126">Enable the soft-delete functionality for this key vault.</span></span>
<span data-ttu-id="07f9d-127">När den är aktive rad kan den inte avaktiveras.</span><span class="sxs-lookup"><span data-stu-id="07f9d-127">Once enabled it cannot be disabled.</span></span>

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

### <span data-ttu-id="07f9d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07f9d-128">-InputObject</span></span>
<span data-ttu-id="07f9d-129">Key valv-objekt.</span><span class="sxs-lookup"><span data-stu-id="07f9d-129">Key vault object.</span></span>

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

### <span data-ttu-id="07f9d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07f9d-130">-ResourceGroupName</span></span>
<span data-ttu-id="07f9d-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="07f9d-131">Name of the resource group.</span></span>

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

### <span data-ttu-id="07f9d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07f9d-132">-ResourceId</span></span>
<span data-ttu-id="07f9d-133">Resurs-ID för huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="07f9d-133">Resource ID of the key vault.</span></span>

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

### <span data-ttu-id="07f9d-134">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="07f9d-134">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="07f9d-135">Anger hur länge borttagna resurser behålls och hur länge ett valv eller ett objekt i det borttagna läget kan tas bort.</span><span class="sxs-lookup"><span data-stu-id="07f9d-135">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="07f9d-136">Standardvärdet är 90 dagar.</span><span class="sxs-lookup"><span data-stu-id="07f9d-136">The default is 90 days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f9d-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="07f9d-137">-VaultName</span></span>
<span data-ttu-id="07f9d-138">Namn på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="07f9d-138">Name of the key vault.</span></span>

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

### <span data-ttu-id="07f9d-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="07f9d-139">-Confirm</span></span>
<span data-ttu-id="07f9d-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="07f9d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07f9d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07f9d-141">-WhatIf</span></span>
<span data-ttu-id="07f9d-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="07f9d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07f9d-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="07f9d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07f9d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f9d-144">CommonParameters</span></span>
<span data-ttu-id="07f9d-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07f9d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f9d-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07f9d-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f9d-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="07f9d-147">INPUTS</span></span>

### <span data-ttu-id="07f9d-148">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="07f9d-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="07f9d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="07f9d-149">System.String</span></span>

## <span data-ttu-id="07f9d-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="07f9d-150">OUTPUTS</span></span>

### <span data-ttu-id="07f9d-151">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="07f9d-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="07f9d-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="07f9d-152">NOTES</span></span>

## <span data-ttu-id="07f9d-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="07f9d-153">RELATED LINKS</span></span>
