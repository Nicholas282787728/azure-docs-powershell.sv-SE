---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupStatus.md
ms.openlocfilehash: 00d7bb2c58abfa466b0c4843eb480b43b08b3d90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757045"
---
# <span data-ttu-id="4de45-101">Get-AzureRmRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="4de45-101">Get-AzureRmRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="4de45-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4de45-102">SYNOPSIS</span></span>
<span data-ttu-id="4de45-103">Kontrollerar om ARM-resursen är säkerhets kopie rad eller inte.</span><span class="sxs-lookup"><span data-stu-id="4de45-103">Checks whether your ARM resource is backed up or not.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4de45-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4de45-104">SYNTAX</span></span>

### <span data-ttu-id="4de45-105">Namn (standard)</span><span class="sxs-lookup"><span data-stu-id="4de45-105">Name (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4de45-106">Et</span><span class="sxs-lookup"><span data-stu-id="4de45-106">Id</span></span>
```
Get-AzureRmRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4de45-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4de45-107">DESCRIPTION</span></span>
<span data-ttu-id="4de45-108">Kommandot returnerar null/tomt om den angivna resursen inte är skyddad under något Recovery Services-valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4de45-108">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="4de45-109">Om den är skyddad returneras relevanta valv uppgifter.</span><span class="sxs-lookup"><span data-stu-id="4de45-109">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="4de45-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4de45-110">EXAMPLES</span></span>

### <span data-ttu-id="4de45-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4de45-111">Example 1</span></span>
```
PS C:\> $status = Get-AzureRmRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzureRmRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzureRmRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="4de45-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4de45-112">PARAMETERS</span></span>

### <span data-ttu-id="4de45-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de45-113">-DefaultProfile</span></span>
<span data-ttu-id="4de45-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4de45-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4de45-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="4de45-115">-Name</span></span>
<span data-ttu-id="4de45-116">Namnet på den Azure-resurs vars ombud måste kontrol leras om det redan skyddas av viss Recovery Services-valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4de45-116">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4de45-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4de45-117">-ResourceGroupName</span></span>
<span data-ttu-id="4de45-118">Namnet på resurs gruppen för Azure-resursen vars ombud måste kontrol leras om det redan skyddas av något RecoveryServices-valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4de45-118">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4de45-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4de45-119">-ResourceId</span></span>
<span data-ttu-id="4de45-120">ID för Azure-resursen vars ombud måste kontrol leras om det redan skyddas av något RecoveryServices-valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4de45-120">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de45-121">– Skriv</span><span class="sxs-lookup"><span data-stu-id="4de45-121">-Type</span></span>
<span data-ttu-id="4de45-122">Namnet på den Azure-resurs vars ombud måste kontrol leras om det redan skyddas av viss Recovery Services-valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4de45-122">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:
Accepted values: AzureVM, AzureFiles

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4de45-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de45-123">CommonParameters</span></span>
<span data-ttu-id="4de45-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4de45-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de45-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4de45-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de45-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4de45-126">INPUTS</span></span>

### <span data-ttu-id="4de45-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4de45-127">System.String</span></span>

## <span data-ttu-id="4de45-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4de45-128">OUTPUTS</span></span>

### <span data-ttu-id="4de45-129">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ResourceBackupStatus</span><span class="sxs-lookup"><span data-stu-id="4de45-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="4de45-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4de45-130">NOTES</span></span>

## <span data-ttu-id="4de45-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4de45-131">RELATED LINKS</span></span>
