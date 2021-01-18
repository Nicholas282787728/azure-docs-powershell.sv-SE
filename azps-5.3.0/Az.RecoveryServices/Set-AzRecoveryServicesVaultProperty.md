---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: e6bd0284d9ce5b5cb6973fce6aae5e16a4c06883
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523126"
---
# <span data-ttu-id="70f8e-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="70f8e-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="70f8e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70f8e-102">SYNOPSIS</span></span>
<span data-ttu-id="70f8e-103">Uppdaterar egenskaper för ett valv.</span><span class="sxs-lookup"><span data-stu-id="70f8e-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="70f8e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70f8e-104">SYNTAX</span></span>

### <span data-ttu-id="70f8e-105">AzureRSVaultSoftDelteParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="70f8e-105">AzureRSVaultSoftDelteParameterSet (Default)</span></span>
```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70f8e-106">AzureRSVaultCMKParameterSet</span><span class="sxs-lookup"><span data-stu-id="70f8e-106">AzureRSVaultCMKParameterSet</span></span>
```
Set-AzRecoveryServicesVaultProperty -EncryptionKeyId <string> -KeyVaultSubscriptionId <string> [-InfrastructureEncryption] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70f8e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70f8e-107">DESCRIPTION</span></span>
<span data-ttu-id="70f8e-108">Cmdleten **set-AzRecoveryServicesVaultProperty** uppdaterar egenskaperna för ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="70f8e-108">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span> <span data-ttu-id="70f8e-109">Denna cmdlet kan användas för att aktivera/inaktivera mjuk borttagning eller för att ange CMK-kryptering för ett valv med två olika parameter uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="70f8e-109">This cmdlet can be used to enable/disable soft delete or set CMK encryption for a vault with two different parameter sets.</span></span> 
<span data-ttu-id="70f8e-110">Egenskapen **SoftDeleteFeatureState** för ett valv kan inaktive ras endast om det inte finns några registrerade behållare i valvet.</span><span class="sxs-lookup"><span data-stu-id="70f8e-110">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span> <span data-ttu-id="70f8e-111">InfrastructurEncryption kan bara anges första gången en användare uppdaterar CMK-valvet.</span><span class="sxs-lookup"><span data-stu-id="70f8e-111">InfrastructurEncryption can only be set the first time a user updates the CMK vault.</span></span>

## <span data-ttu-id="70f8e-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70f8e-112">EXAMPLES</span></span>

### <span data-ttu-id="70f8e-113">Exempel 1: uppdatera SoftDeleteFeatureState för ett valv</span><span class="sxs-lookup"><span data-stu-id="70f8e-113">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="70f8e-114">Det första kommandot får ett valv objekt och lagrar det sedan i $vault variabel.</span><span class="sxs-lookup"><span data-stu-id="70f8e-114">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="70f8e-115">Det andra kommandot uppdaterar egenskapen SoftDeleteFeatureState för valvet till tillståndet "Enabled".</span><span class="sxs-lookup"><span data-stu-id="70f8e-115">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

### <span data-ttu-id="70f8e-116">Exempel 2: uppdatera CMK kryptering av ett valv</span><span class="sxs-lookup"><span data-stu-id="70f8e-116">Example 2: Update CMK encryption of a vault</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $keyVault = Get-AzKeyVault -VaultName "keyVaultName" -ResourceGroupName "RGName" 
PS C:\> $key = Get-AzKeyVaultKey -VaultName "keyVaultName" -Name "keyName" 
PS C:\> Set-AzRecoveryServicesVaultProperty -EncryptionKeyId $key.ID -KeyVaultSubscriptionId "f870818k-5h28-4t48-8961-37458592348r" -InfrastructureEncryption -VaultId $vault.ID
```

<span data-ttu-id="70f8e-117">Den första cmdleten får RSVault att uppdatera krypterings egenskaper.</span><span class="sxs-lookup"><span data-stu-id="70f8e-117">First cmdlet gets the RSVault to update encryption properties.</span></span> <span data-ttu-id="70f8e-118">Den andra cmdleten får ett Azure Key-valv.</span><span class="sxs-lookup"><span data-stu-id="70f8e-118">Second cmdlet gets the azure key vault.</span></span> <span data-ttu-id="70f8e-119">Den tredje cmdleten hämtar tangenten från Key Vault.</span><span class="sxs-lookup"><span data-stu-id="70f8e-119">Third cmdlet get the key from the key vault.</span></span>
<span data-ttu-id="70f8e-120">Fjärde cmdleten uppdaterar kund hanterad krypterings nycklar i RSVault.</span><span class="sxs-lookup"><span data-stu-id="70f8e-120">Fourth cmdlet updates the customer managed encryption key within the RSVault.</span></span> <span data-ttu-id="70f8e-121">Use-InfrastructureEncryption parameter för att aktivera infrastruktur kryptering för den första uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="70f8e-121">Use -InfrastructureEncryption param to enable infrastructure encryption for the first time update.</span></span> 

## <span data-ttu-id="70f8e-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70f8e-122">PARAMETERS</span></span>

### <span data-ttu-id="70f8e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70f8e-123">-DefaultProfile</span></span>
<span data-ttu-id="70f8e-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70f8e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70f8e-125">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="70f8e-125">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="70f8e-126">SoftDeleteFeatureState av Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="70f8e-126">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f8e-127">-EncryptionKeyId</span><span class="sxs-lookup"><span data-stu-id="70f8e-127">-EncryptionKeyId</span></span>
<span data-ttu-id="70f8e-128">KeyId som används för CMK.</span><span class="sxs-lookup"><span data-stu-id="70f8e-128">KeyId of the encryption key to be used for CMK.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: KeyID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f8e-129">-KeyVaultSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="70f8e-129">-KeyVaultSubscriptionId</span></span>
<span data-ttu-id="70f8e-130">Abonnemangs-ID för huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="70f8e-130">Subscription Id of the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SubscriptionID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f8e-131">-InfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="70f8e-131">-InfrastructureEncryption</span></span>
<span data-ttu-id="70f8e-132">Aktiverar infrastruktur kryptering i det här valvet.</span><span class="sxs-lookup"><span data-stu-id="70f8e-132">Enables infrastructure encryption on this vault.</span></span> <span data-ttu-id="70f8e-133">Infrastruktur kryptering måste aktive ras när kryptering konfigureras.</span><span class="sxs-lookup"><span data-stu-id="70f8e-133">Infrastructure encryption must be enabled when configuring encryption.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f8e-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="70f8e-134">-VaultId</span></span>
<span data-ttu-id="70f8e-135">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="70f8e-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="70f8e-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="70f8e-136">-Confirm</span></span>
<span data-ttu-id="70f8e-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="70f8e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70f8e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70f8e-138">-WhatIf</span></span>
<span data-ttu-id="70f8e-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="70f8e-139">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="70f8e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f8e-140">CommonParameters</span></span>
<span data-ttu-id="70f8e-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70f8e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f8e-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70f8e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f8e-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70f8e-143">INPUTS</span></span>

### <span data-ttu-id="70f8e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="70f8e-144">System.String</span></span>

### <span data-ttu-id="70f8e-145">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="70f8e-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="70f8e-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70f8e-146">OUTPUTS</span></span>

### <span data-ttu-id="70f8e-147">Microsoft. Azure. Management. RecoveryServices. backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="70f8e-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="70f8e-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70f8e-148">NOTES</span></span>

## <span data-ttu-id="70f8e-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70f8e-149">RELATED LINKS</span></span>

[<span data-ttu-id="70f8e-150">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="70f8e-150">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="70f8e-151">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="70f8e-151">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)
