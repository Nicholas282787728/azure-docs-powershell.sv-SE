---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/set-azurermrecoveryservicesbackupproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
ms.openlocfilehash: 7fa55bd306a1cbe04ddf3af63a66682a0fa17f1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573928"
---
# <span data-ttu-id="57149-101">Set-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="57149-101">Set-AzureRmRecoveryServicesBackupProperties</span></span>

## <span data-ttu-id="57149-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57149-102">SYNOPSIS</span></span>
<span data-ttu-id="57149-103">Anger egenskaper för säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="57149-103">Sets the properties for backup management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57149-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57149-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProperties -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57149-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57149-105">DESCRIPTION</span></span>
<span data-ttu-id="57149-106">Cmdleten **set-AzureRmRecoveryServicesBackupProperties** anger egenskaper för säkerhets kopierings lagring för ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="57149-106">The **Set-AzureRmRecoveryServicesBackupProperties** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="57149-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57149-107">EXAMPLES</span></span>

### <span data-ttu-id="57149-108">Exempel 1: Ange redundant lagrings utrymme för ett valv</span><span class="sxs-lookup"><span data-stu-id="57149-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzureRmRecoveryServicesBackupProperties -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="57149-109">Det första kommandot får valvet med namnet TestVault och lagrar det sedan i variabeln $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="57149-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="57149-110">Det andra kommandot ställer in redundans för säkerhets kopiering för $Vault 01 till redundant.</span><span class="sxs-lookup"><span data-stu-id="57149-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="57149-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57149-111">PARAMETERS</span></span>

### <span data-ttu-id="57149-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="57149-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="57149-113">Anger typen av redundans för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="57149-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: AzureRmRecoveryServicesBackupStorageRedundancyType
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57149-114">-Valv</span><span class="sxs-lookup"><span data-stu-id="57149-114">-Vault</span></span>
<span data-ttu-id="57149-115">Anger namnet på valvet.</span><span class="sxs-lookup"><span data-stu-id="57149-115">Specifies the name of the vault.</span></span>
<span data-ttu-id="57149-116">Valvet måste vara ett **AzureRmRecoveryServicesVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="57149-116">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57149-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="57149-117">-Confirm</span></span>
<span data-ttu-id="57149-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="57149-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57149-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57149-119">-WhatIf</span></span>
<span data-ttu-id="57149-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="57149-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57149-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="57149-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57149-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57149-122">-DefaultProfile</span></span>
<span data-ttu-id="57149-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="57149-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57149-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57149-124">CommonParameters</span></span>
<span data-ttu-id="57149-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57149-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57149-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57149-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57149-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57149-127">INPUTS</span></span>

### <span data-ttu-id="57149-128">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="57149-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="57149-129">Parametrar: valv (ByValue)</span><span class="sxs-lookup"><span data-stu-id="57149-129">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="57149-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57149-130">OUTPUTS</span></span>

### <span data-ttu-id="57149-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="57149-131">System.Void</span></span>

## <span data-ttu-id="57149-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57149-132">NOTES</span></span>

## <span data-ttu-id="57149-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57149-133">RELATED LINKS</span></span>

[<span data-ttu-id="57149-134">Get-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="57149-134">Get-AzureRmRecoveryServicesBackupProperties</span></span>](./Get-AzureRmRecoveryServicesBackupProperties.md)

[<span data-ttu-id="57149-135">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="57149-135">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)


