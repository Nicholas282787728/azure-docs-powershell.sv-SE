---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: a9bd1eead98a7afb06e1f5b480f8a65fc5079bd4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091247"
---
# <span data-ttu-id="50c1d-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="50c1d-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="50c1d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50c1d-102">SYNOPSIS</span></span>
<span data-ttu-id="50c1d-103">Uppdaterar egenskaper för ett valv.</span><span class="sxs-lookup"><span data-stu-id="50c1d-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="50c1d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50c1d-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50c1d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50c1d-105">DESCRIPTION</span></span>
<span data-ttu-id="50c1d-106">Cmdleten **set-AzRecoveryServicesVaultProperty** uppdaterar egenskaperna för ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="50c1d-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="50c1d-107">Du kan använda cmdleten **set-AzRecoveryServicesVaultProperty** för att hämta de aktuella egenskaperna för ett valv.</span><span class="sxs-lookup"><span data-stu-id="50c1d-107">You can use **Set-AzRecoveryServicesVaultProperty** cmdlet to get the current properties of a vault.</span></span>
<span data-ttu-id="50c1d-108">Denna cmdlet **SoftDeleteFeatureState** egenskap för ett valv kan aktive ras när som helst.</span><span class="sxs-lookup"><span data-stu-id="50c1d-108">Using this cmdlet **SoftDeleteFeatureState** property of a vault can be enabled at any point of time.</span></span>
<span data-ttu-id="50c1d-109">Egenskapen **SoftDeleteFeatureState** för ett valv kan inaktive ras endast om det inte finns några registrerade behållare i valvet.</span><span class="sxs-lookup"><span data-stu-id="50c1d-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>
<span data-ttu-id="50c1d-110">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50c1d-110">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="50c1d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50c1d-111">EXAMPLES</span></span>

### <span data-ttu-id="50c1d-112">Exempel 1: uppdatera SoftDeleteFeatureState för ett valv</span><span class="sxs-lookup"><span data-stu-id="50c1d-112">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="50c1d-113">Det första kommandot får ett valv objekt och lagrar det sedan i $vault variabel.</span><span class="sxs-lookup"><span data-stu-id="50c1d-113">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="50c1d-114">Det andra kommandot uppdaterar egenskapen SoftDeleteFeatureState för valvet till tillståndet "Enabled".</span><span class="sxs-lookup"><span data-stu-id="50c1d-114">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="50c1d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50c1d-115">PARAMETERS</span></span>

### <span data-ttu-id="50c1d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50c1d-116">-DefaultProfile</span></span>
<span data-ttu-id="50c1d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="50c1d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50c1d-118">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="50c1d-118">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="50c1d-119">SoftDeleteFeatureState av Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="50c1d-119">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="50c1d-120">-VaultId</span><span class="sxs-lookup"><span data-stu-id="50c1d-120">-VaultId</span></span>
<span data-ttu-id="50c1d-121">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="50c1d-121">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="50c1d-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="50c1d-122">-Confirm</span></span>
<span data-ttu-id="50c1d-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50c1d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50c1d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50c1d-124">-WhatIf</span></span>
<span data-ttu-id="50c1d-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="50c1d-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50c1d-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="50c1d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50c1d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50c1d-127">CommonParameters</span></span>
<span data-ttu-id="50c1d-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50c1d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50c1d-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50c1d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50c1d-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50c1d-130">INPUTS</span></span>

### <span data-ttu-id="50c1d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="50c1d-131">System.String</span></span>

### <span data-ttu-id="50c1d-132">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="50c1d-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="50c1d-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50c1d-133">OUTPUTS</span></span>

### <span data-ttu-id="50c1d-134">Microsoft. Azure. Management. RecoveryServices. backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="50c1d-134">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="50c1d-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50c1d-135">NOTES</span></span>

## <span data-ttu-id="50c1d-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50c1d-136">RELATED LINKS</span></span>

[<span data-ttu-id="50c1d-137">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="50c1d-137">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="50c1d-138">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="50c1d-138">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


