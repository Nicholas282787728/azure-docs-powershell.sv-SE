---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 7717aaa76efba736015a1cf762c95af440b28218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578728"
---
# <span data-ttu-id="1274b-101">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1274b-101">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="1274b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1274b-102">SYNOPSIS</span></span>
<span data-ttu-id="1274b-103">Skapar eller uppdaterar ImmutabilityPolicy för en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="1274b-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1274b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1274b-104">SYNTAX</span></span>

### <span data-ttu-id="1274b-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="1274b-105">AccountName (Default)</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> -ImmutabilityPeriod <Int32> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1274b-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="1274b-106">ExtendAccountName</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1274b-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="1274b-107">AccountObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1274b-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="1274b-108">ExtendAccountObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1274b-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="1274b-109">ContainerObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1274b-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="1274b-110">ExtendContainerObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1274b-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="1274b-111">ImmutabilityPolicyObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1274b-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="1274b-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1274b-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1274b-113">DESCRIPTION</span></span>
<span data-ttu-id="1274b-114">Cmdleten **set-AzureRmStorageContainerImmutabilityPolicy** skapar eller uppdaterar ImmutabilityPolicy för en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="1274b-114">The **Set-AzureRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="1274b-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1274b-115">EXAMPLES</span></span>

### <span data-ttu-id="1274b-116">Exempel 1: skapa eller uppdatera ImmutabilityPolicy för en lagrings-behållare med lagrings konto namn och container namn</span><span class="sxs-lookup"><span data-stu-id="1274b-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10 
```

<span data-ttu-id="1274b-117">Det här kommandot skapar eller uppdaterar ImmutabilityPolicy för en lagrings-behållare med lagrings konto namn och container namn.</span><span class="sxs-lookup"><span data-stu-id="1274b-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="1274b-118">Exempel 2: Förläng ImmutabilityPolicy av en lagrings-behållare med lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="1274b-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="1274b-119">Det här kommandot utökar ImmutabilityPolicy för en lagrings-behållare med lagrings konto objekt.</span><span class="sxs-lookup"><span data-stu-id="1274b-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="1274b-120">Utökade ImmutabilityPolicy kan bara köras när ImmutabilityPolicy är låst.</span><span class="sxs-lookup"><span data-stu-id="1274b-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="1274b-121">Exempel 3: uppdatera ImmutabilityPolicyof en BLOB-behållare för lagring</span><span class="sxs-lookup"><span data-stu-id="1274b-121">Example 3: Update ImmutabilityPolicyof a Storage blob container</span></span> 
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
```

<span data-ttu-id="1274b-122">Det här kommandot uppdaterar ImmutabilityPolicy för en lagrings-behållare med lagrings behållar objekt 2 gånger, först till ImmutabilityPeriod 12 dagar utan etag, och sedan till ImmutabilityPeriod nio dagar med etag.</span><span class="sxs-lookup"><span data-stu-id="1274b-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 2 times, first to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag.</span></span>

### <span data-ttu-id="1274b-123">Exempel 4: Förläng ImmutabilityPolicy av en lagrings-behållare med ImmutabilityPolicy-objekt</span><span class="sxs-lookup"><span data-stu-id="1274b-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzureRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="1274b-124">Det här kommandot utökar ImmutabilityPolicy för en lagrings-behållare med ImmutabilityPolicy-objekt.</span><span class="sxs-lookup"><span data-stu-id="1274b-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="1274b-125">Utökade ImmutabilityPolicy kan bara köras när ImmutabilityPolicy är låst.</span><span class="sxs-lookup"><span data-stu-id="1274b-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="1274b-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1274b-126">PARAMETERS</span></span>

### <span data-ttu-id="1274b-127">-Container</span><span class="sxs-lookup"><span data-stu-id="1274b-127">-Container</span></span>
<span data-ttu-id="1274b-128">Container-objekt</span><span class="sxs-lookup"><span data-stu-id="1274b-128">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1274b-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="1274b-129">-ContainerName</span></span>
<span data-ttu-id="1274b-130">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="1274b-130">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1274b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1274b-131">-DefaultProfile</span></span>
<span data-ttu-id="1274b-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1274b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1274b-133">-Etag</span><span class="sxs-lookup"><span data-stu-id="1274b-133">-Etag</span></span>
<span data-ttu-id="1274b-134">Immutability policy etag.</span><span class="sxs-lookup"><span data-stu-id="1274b-134">Immutability policy etag.</span></span> <span data-ttu-id="1274b-135">Om-ExtendPolicy inte anges är etag valfri; Else etag krävs.</span><span class="sxs-lookup"><span data-stu-id="1274b-135">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1274b-136">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="1274b-136">-ExtendPolicy</span></span>
<span data-ttu-id="1274b-137">Ange ExtendPolicy för att utöka en befintlig ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="1274b-137">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="1274b-138">När ImmutabilityPolicy är låst kan den bara utökas.</span><span class="sxs-lookup"><span data-stu-id="1274b-138">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

```yaml
Type: SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1274b-139">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="1274b-139">-ImmutabilityPeriod</span></span>
<span data-ttu-id="1274b-140">Immutability-perioden sedan den skapades i dagar.</span><span class="sxs-lookup"><span data-stu-id="1274b-140">Immutability period since creation in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1274b-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1274b-141">-InputObject</span></span>
<span data-ttu-id="1274b-142">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="1274b-142">Container Name</span></span>

```yaml
Type: PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1274b-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1274b-143">-ResourceGroupName</span></span>
<span data-ttu-id="1274b-144">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="1274b-144">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1274b-145">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1274b-145">-StorageAccount</span></span>
<span data-ttu-id="1274b-146">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="1274b-146">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1274b-147">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1274b-147">-StorageAccountName</span></span>
<span data-ttu-id="1274b-148">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="1274b-148">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1274b-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1274b-149">-Confirm</span></span>
<span data-ttu-id="1274b-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1274b-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1274b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1274b-151">-WhatIf</span></span>
<span data-ttu-id="1274b-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1274b-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1274b-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1274b-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1274b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1274b-154">CommonParameters</span></span>
<span data-ttu-id="1274b-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1274b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1274b-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1274b-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1274b-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1274b-157">INPUTS</span></span>

### <span data-ttu-id="1274b-158">System. String</span><span class="sxs-lookup"><span data-stu-id="1274b-158">System.String</span></span>
<span data-ttu-id="1274b-159">Microsoft. Azure. commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1274b-159">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="1274b-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1274b-160">OUTPUTS</span></span>

### <span data-ttu-id="1274b-161">Microsoft. Azure. commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1274b-161">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="1274b-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1274b-162">NOTES</span></span>

## <span data-ttu-id="1274b-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1274b-163">RELATED LINKS</span></span>

