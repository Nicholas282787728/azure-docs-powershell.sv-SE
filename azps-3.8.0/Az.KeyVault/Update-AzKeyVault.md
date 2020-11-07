---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 8932402fb9e4e6b27f284313bfddc764192c5e93
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926605"
---
# <span data-ttu-id="c9d58-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="c9d58-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="c9d58-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c9d58-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d58-103">Uppdatera tillståndet för ett Azure Key-valv.</span><span class="sxs-lookup"><span data-stu-id="c9d58-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="c9d58-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c9d58-104">SYNTAX</span></span>

### <span data-ttu-id="c9d58-105">UpdateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c9d58-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9d58-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9d58-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9d58-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9d58-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9d58-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c9d58-108">DESCRIPTION</span></span>
<span data-ttu-id="c9d58-109">Denna cmdlet uppdaterar tillståndet för ett Azure Key-valv.</span><span class="sxs-lookup"><span data-stu-id="c9d58-109">This cmdlet updates the state of an Azure key vault.</span></span>
<span data-ttu-id="c9d58-110">Observera att om du uppdaterar vissa egenskaper är en irreversibl åtgärd, till exempel när en mjuk borttagning har Aktiver ATS kan den inte inaktive ras längre.</span><span class="sxs-lookup"><span data-stu-id="c9d58-110">Please note updating some of the properties is an irreversible action, for example once soft delete has been enabled, it cannot be disabled anymore.</span></span>

## <span data-ttu-id="c9d58-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c9d58-111">EXAMPLES</span></span>

### <span data-ttu-id="c9d58-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c9d58-112">Example 1</span></span>
```powershell
PS C:\> Update-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName -EnableSoftDelete
```

<span data-ttu-id="c9d58-113">Aktiverar mjuk borttagning på Key Vault som heter `$keyVaultName` i resurs gruppen `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="c9d58-113">Enables soft delete on the key vault named `$keyVaultName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="c9d58-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c9d58-114">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="c9d58-115">Aktiverar rensa skydd med rör-syntax.</span><span class="sxs-lookup"><span data-stu-id="c9d58-115">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="c9d58-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c9d58-116">PARAMETERS</span></span>

### <span data-ttu-id="c9d58-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d58-117">-DefaultProfile</span></span>
<span data-ttu-id="c9d58-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c9d58-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d58-119">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="c9d58-119">-EnablePurgeProtection</span></span>
<span data-ttu-id="c9d58-120">Aktivera funktionerna för rensnings skydd för det här nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="c9d58-120">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="c9d58-121">När den är aktive rad kan den inte avaktiveras.</span><span class="sxs-lookup"><span data-stu-id="c9d58-121">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="c9d58-122">Borttagning krävs för att den ska vara aktive rad.</span><span class="sxs-lookup"><span data-stu-id="c9d58-122">It requires soft-delete to be turned on.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d58-123">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="c9d58-123">-EnableSoftDelete</span></span>
<span data-ttu-id="c9d58-124">Aktivera funktionerna för mjuk borttagning för det här nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="c9d58-124">Enable the soft-delete functionality for this key vault.</span></span>
<span data-ttu-id="c9d58-125">När den är aktive rad kan den inte avaktiveras.</span><span class="sxs-lookup"><span data-stu-id="c9d58-125">Once enabled it cannot be disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d58-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9d58-126">-InputObject</span></span>
<span data-ttu-id="c9d58-127">Key valv-objekt.</span><span class="sxs-lookup"><span data-stu-id="c9d58-127">Key vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d58-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9d58-128">-ResourceGroupName</span></span>
<span data-ttu-id="c9d58-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c9d58-129">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d58-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9d58-130">-ResourceId</span></span>
<span data-ttu-id="c9d58-131">Resurs-ID för huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="c9d58-131">Resource ID of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d58-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c9d58-132">-VaultName</span></span>
<span data-ttu-id="c9d58-133">Namn på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="c9d58-133">Name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d58-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c9d58-134">-Confirm</span></span>
<span data-ttu-id="c9d58-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c9d58-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9d58-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9d58-136">-WhatIf</span></span>
<span data-ttu-id="c9d58-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c9d58-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9d58-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c9d58-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9d58-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d58-139">CommonParameters</span></span>
<span data-ttu-id="c9d58-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9d58-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d58-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9d58-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d58-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c9d58-142">INPUTS</span></span>

### <span data-ttu-id="c9d58-143">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="c9d58-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="c9d58-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c9d58-144">System.String</span></span>

## <span data-ttu-id="c9d58-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c9d58-145">OUTPUTS</span></span>

### <span data-ttu-id="c9d58-146">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="c9d58-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="c9d58-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c9d58-147">NOTES</span></span>

## <span data-ttu-id="c9d58-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c9d58-148">RELATED LINKS</span></span>
