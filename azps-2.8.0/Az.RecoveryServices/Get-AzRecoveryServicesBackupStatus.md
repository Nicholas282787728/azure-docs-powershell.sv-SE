---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
ms.openlocfilehash: cd3e3e2ad33cb01935a2594571145f0667c9a3e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919727"
---
# <span data-ttu-id="546a1-101">Get-AzRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="546a1-101">Get-AzRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="546a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="546a1-102">SYNOPSIS</span></span>
<span data-ttu-id="546a1-103">Kontrollerar om ARM-resursen är säkerhets kopie rad eller inte.</span><span class="sxs-lookup"><span data-stu-id="546a1-103">Checks whether your ARM resource is backed up or not.</span></span>

## <span data-ttu-id="546a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="546a1-104">SYNTAX</span></span>

### <span data-ttu-id="546a1-105">Namn (standard)</span><span class="sxs-lookup"><span data-stu-id="546a1-105">Name (Default)</span></span>
```
Get-AzRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="546a1-106">IdWorkload</span><span class="sxs-lookup"><span data-stu-id="546a1-106">IdWorkload</span></span>
```
Get-AzRecoveryServicesBackupStatus -Type <String> -ResourceId <String> -ProtectableObjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="546a1-107">Et</span><span class="sxs-lookup"><span data-stu-id="546a1-107">Id</span></span>
```
Get-AzRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="546a1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="546a1-108">DESCRIPTION</span></span>
<span data-ttu-id="546a1-109">Kommandot returnerar null/tomt om den angivna resursen inte är skyddad under något Recovery Services-valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="546a1-109">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="546a1-110">Om den är skyddad returneras relevanta valv uppgifter.</span><span class="sxs-lookup"><span data-stu-id="546a1-110">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="546a1-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="546a1-111">EXAMPLES</span></span>

### <span data-ttu-id="546a1-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="546a1-112">Example 1</span></span>
```
PS C:\> $status = Get-AzRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="546a1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="546a1-113">PARAMETERS</span></span>

### <span data-ttu-id="546a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="546a1-114">-DefaultProfile</span></span>
<span data-ttu-id="546a1-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="546a1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="546a1-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="546a1-116">-Name</span></span>
<span data-ttu-id="546a1-117">Namnet på den Azure-resurs vars ombud måste kontrol leras om det redan skyddas av viss Recovery Services-valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="546a1-117">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

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

### <span data-ttu-id="546a1-118">-ProtectableObjectName</span><span class="sxs-lookup"><span data-stu-id="546a1-118">-ProtectableObjectName</span></span>
<span data-ttu-id="546a1-119">Namnet på den Azure-resurs vars ombud måste kontrol leras om det redan skyddas av viss Recovery Services-valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="546a1-119">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: IdWorkload
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546a1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="546a1-120">-ResourceGroupName</span></span>
<span data-ttu-id="546a1-121">Namnet på resurs gruppen för Azure-resursen vars ombud måste kontrol leras om det redan skyddas av något RecoveryServices-valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="546a1-121">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="546a1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="546a1-122">-ResourceId</span></span>
<span data-ttu-id="546a1-123">ID för Azure-resursen vars ombud måste kontrol leras om det redan skyddas av något RecoveryServices-valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="546a1-123">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: IdWorkload, Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546a1-124">– Skriv</span><span class="sxs-lookup"><span data-stu-id="546a1-124">-Type</span></span>
<span data-ttu-id="546a1-125">Namnet på den Azure-resurs vars ombud måste kontrol leras om det redan skyddas av viss Recovery Services-valv i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="546a1-125">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, IdWorkload
Aliases:
Accepted values: AzureVM, AzureFiles

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="546a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="546a1-126">CommonParameters</span></span>
<span data-ttu-id="546a1-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="546a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="546a1-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="546a1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="546a1-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="546a1-129">INPUTS</span></span>

### <span data-ttu-id="546a1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="546a1-130">System.String</span></span>

## <span data-ttu-id="546a1-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="546a1-131">OUTPUTS</span></span>

### <span data-ttu-id="546a1-132">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ResourceBackupStatus</span><span class="sxs-lookup"><span data-stu-id="546a1-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="546a1-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="546a1-133">NOTES</span></span>

## <span data-ttu-id="546a1-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="546a1-134">RELATED LINKS</span></span>
