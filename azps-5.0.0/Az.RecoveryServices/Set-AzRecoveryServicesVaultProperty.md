---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4b34bdf2357b389081297df8f49745127953985b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263427"
---
# <span data-ttu-id="8d170-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="8d170-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="8d170-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d170-102">SYNOPSIS</span></span>
<span data-ttu-id="8d170-103">Uppdaterar egenskaper för ett valv.</span><span class="sxs-lookup"><span data-stu-id="8d170-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="8d170-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d170-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d170-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d170-105">DESCRIPTION</span></span>
<span data-ttu-id="8d170-106">Cmdleten **set-AzRecoveryServicesVaultProperty** uppdaterar egenskaperna för ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="8d170-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="8d170-107">Denna cmdlet returnerar de uppdaterade valv egenskaperna efter den aktuella åtgärden.</span><span class="sxs-lookup"><span data-stu-id="8d170-107">This cmdlet returns the updated vault properties after the current set operation.</span></span>
<span data-ttu-id="8d170-108">Om du använder dessa cmdlet-egenskaper i valvet, till exempel mjuk borttagning, kan du aktivera dem när som helst.</span><span class="sxs-lookup"><span data-stu-id="8d170-108">Using this cmdlet properties of vault such as soft-delete can be enabled at any point of time.</span></span>
<span data-ttu-id="8d170-109">Egenskapen **SoftDeleteFeatureState** för ett valv kan inaktive ras endast om det inte finns några registrerade behållare i valvet.</span><span class="sxs-lookup"><span data-stu-id="8d170-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>

## <span data-ttu-id="8d170-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d170-110">EXAMPLES</span></span>

### <span data-ttu-id="8d170-111">Exempel 1: uppdatera SoftDeleteFeatureState för ett valv</span><span class="sxs-lookup"><span data-stu-id="8d170-111">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="8d170-112">Det första kommandot får ett valv objekt och lagrar det sedan i $vault variabel.</span><span class="sxs-lookup"><span data-stu-id="8d170-112">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="8d170-113">Det andra kommandot uppdaterar egenskapen SoftDeleteFeatureState för valvet till tillståndet "Enabled".</span><span class="sxs-lookup"><span data-stu-id="8d170-113">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="8d170-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d170-114">PARAMETERS</span></span>

### <span data-ttu-id="8d170-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d170-115">-DefaultProfile</span></span>
<span data-ttu-id="8d170-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8d170-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d170-117">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="8d170-117">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="8d170-118">SoftDeleteFeatureState av Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="8d170-118">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8d170-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8d170-119">-VaultId</span></span>
<span data-ttu-id="8d170-120">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="8d170-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8d170-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8d170-121">-Confirm</span></span>
<span data-ttu-id="8d170-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8d170-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d170-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d170-123">-WhatIf</span></span>
<span data-ttu-id="8d170-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8d170-124">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="8d170-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d170-125">CommonParameters</span></span>
<span data-ttu-id="8d170-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d170-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d170-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d170-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d170-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d170-128">INPUTS</span></span>

### <span data-ttu-id="8d170-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8d170-129">System.String</span></span>

### <span data-ttu-id="8d170-130">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="8d170-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="8d170-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d170-131">OUTPUTS</span></span>

### <span data-ttu-id="8d170-132">Microsoft. Azure. Management. RecoveryServices. backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="8d170-132">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="8d170-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d170-133">NOTES</span></span>

## <span data-ttu-id="8d170-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d170-134">RELATED LINKS</span></span>

[<span data-ttu-id="8d170-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8d170-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="8d170-136">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="8d170-136">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


