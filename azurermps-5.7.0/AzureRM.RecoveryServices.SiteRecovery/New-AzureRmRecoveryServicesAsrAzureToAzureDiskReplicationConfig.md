---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 542e75ed0e6531f5778f9793b678b42f953c15d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573380"
---
# <span data-ttu-id="16ce3-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="16ce3-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="16ce3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="16ce3-103">Skapar ett disk kart objekt för virtuella Azure Virtual Machine-diskar att replikeras.</span><span class="sxs-lookup"><span data-stu-id="16ce3-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16ce3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16ce3-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16ce3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16ce3-105">DESCRIPTION</span></span>
<span data-ttu-id="16ce3-106">Skapar ett disk kart objekt som mappar en virtuell Azure-dator-disk till det lagrings konto och mål lagrings konto (återställnings område) som ska användas för att replikera disken.</span><span class="sxs-lookup"><span data-stu-id="16ce3-106">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="16ce3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16ce3-107">EXAMPLES</span></span>

### <span data-ttu-id="16ce3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="16ce3-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="16ce3-109">Skapa ett disk kart objekt för virtuella Azure Virtual Machine-diskar att replikeras. Används under Azure to Azure-Aktiveradare och skydds åtgärd.</span><span class="sxs-lookup"><span data-stu-id="16ce3-109">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="16ce3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16ce3-110">PARAMETERS</span></span>

### <span data-ttu-id="16ce3-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="16ce3-111">-Confirm</span></span>
<span data-ttu-id="16ce3-112">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="16ce3-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16ce3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ce3-113">-DefaultProfile</span></span>
<span data-ttu-id="16ce3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="16ce3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16ce3-115">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="16ce3-115">-LogStorageAccountId</span></span>
<span data-ttu-id="16ce3-116">Anger det ID för logg-eller cache-minnet som ska användas för att lagra loggar.</span><span class="sxs-lookup"><span data-stu-id="16ce3-116">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16ce3-117">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="16ce3-117">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="16ce3-118">Anger ID för det Azure Storage-konto som ska replikeras till.</span><span class="sxs-lookup"><span data-stu-id="16ce3-118">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16ce3-119">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="16ce3-119">-VhdUri</span></span>
<span data-ttu-id="16ce3-120">Ange VHD URI för den disk som den här mappningen motsvarar.</span><span class="sxs-lookup"><span data-stu-id="16ce3-120">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16ce3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16ce3-121">-WhatIf</span></span>
<span data-ttu-id="16ce3-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="16ce3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16ce3-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="16ce3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16ce3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ce3-124">CommonParameters</span></span>
<span data-ttu-id="16ce3-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16ce3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ce3-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16ce3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ce3-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16ce3-127">INPUTS</span></span>

### <span data-ttu-id="16ce3-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="16ce3-128">None</span></span>

## <span data-ttu-id="16ce3-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16ce3-129">OUTPUTS</span></span>

### <span data-ttu-id="16ce3-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="16ce3-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="16ce3-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16ce3-131">NOTES</span></span>

## <span data-ttu-id="16ce3-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16ce3-132">RELATED LINKS</span></span>
