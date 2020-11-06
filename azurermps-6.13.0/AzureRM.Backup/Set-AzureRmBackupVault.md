---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: D57C32D1-EB4F-495E-A11B-3B4066E8C552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
ms.openlocfilehash: edb119484d397241b786ff9476b688e150ed3c6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575332"
---
# <span data-ttu-id="01a51-101">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="01a51-101">Set-AzureRmBackupVault</span></span>

## <span data-ttu-id="01a51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="01a51-102">SYNOPSIS</span></span>
<span data-ttu-id="01a51-103">Ändrar lagrings typen för ett säkerhets kopierings valv.</span><span class="sxs-lookup"><span data-stu-id="01a51-103">Changes the storage type of a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01a51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="01a51-104">SYNTAX</span></span>

```
Set-AzureRmBackupVault [[-Storage] <AzureBackupVaultStorageType>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01a51-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="01a51-105">DESCRIPTION</span></span>
<span data-ttu-id="01a51-106">Cmdleten **set-AzureRmBackupVault** ändrar lagrings typen för ett Azure Backup-valv.</span><span class="sxs-lookup"><span data-stu-id="01a51-106">The **Set-AzureRmBackupVault** cmdlet changes the storage type of an Azure Backup vault.</span></span>
<span data-ttu-id="01a51-107">Du kan inte ändra andra egenskaper för ett valv.</span><span class="sxs-lookup"><span data-stu-id="01a51-107">You cannot modify other properties of a vault.</span></span>

## <span data-ttu-id="01a51-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="01a51-108">EXAMPLES</span></span>

### <span data-ttu-id="01a51-109">Exempel 1: ändra lagrings utrymmet för ett befintligt valv</span><span class="sxs-lookup"><span data-stu-id="01a51-109">Example 1: Change the storage for an existing vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Set-AzureRmBackupVault -Storage LocallyRedundant
```

<span data-ttu-id="01a51-110">Det här kommandot får Azure Backup-valvet med namnet Vault03 med hjälp av cmdleten **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="01a51-110">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="01a51-111">Kommandot skickar detta valv till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="01a51-111">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="01a51-112">Den aktuella cmdleten ändrar lagrings typen till LocallyRedundant.</span><span class="sxs-lookup"><span data-stu-id="01a51-112">The current cmdlet changes the storage type to LocallyRedundant.</span></span>

## <span data-ttu-id="01a51-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="01a51-113">PARAMETERS</span></span>

### <span data-ttu-id="01a51-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01a51-114">-DefaultProfile</span></span>
<span data-ttu-id="01a51-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="01a51-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01a51-116">-Lagring</span><span class="sxs-lookup"><span data-stu-id="01a51-116">-Storage</span></span>
<span data-ttu-id="01a51-117">Anger lagrings typen för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="01a51-117">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="01a51-118">De acceptabla värdena för den här parametern är: LocallyRedundant och är bevarade.</span><span class="sxs-lookup"><span data-stu-id="01a51-118">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a51-119">-Valv</span><span class="sxs-lookup"><span data-stu-id="01a51-119">-Vault</span></span>
<span data-ttu-id="01a51-120">Anger ett säkerhets kopierings valv som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="01a51-120">Specifies a Backup vault that this cmdlet modifies.</span></span>
<span data-ttu-id="01a51-121">Använd Get-AzureRmBackupVault cmdlet för att få ett **AzureRmBackupVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="01a51-121">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01a51-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01a51-122">CommonParameters</span></span>
<span data-ttu-id="01a51-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01a51-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01a51-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01a51-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01a51-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="01a51-125">INPUTS</span></span>

### <span data-ttu-id="01a51-126">Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="01a51-126">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="01a51-127">Parametrar: valv (ByValue)</span><span class="sxs-lookup"><span data-stu-id="01a51-127">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="01a51-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="01a51-128">OUTPUTS</span></span>

### <span data-ttu-id="01a51-129">Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="01a51-129">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>

## <span data-ttu-id="01a51-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="01a51-130">NOTES</span></span>
* <span data-ttu-id="01a51-131">När du registrerar den första servern eller virtuella datorn för ett valv är lagrings typen låst.</span><span class="sxs-lookup"><span data-stu-id="01a51-131">When you register the first server or virtual machine for a vault, the storage type is locked.</span></span> <span data-ttu-id="01a51-132">Därefter kan du inte ändra lagrings typen.</span><span class="sxs-lookup"><span data-stu-id="01a51-132">Subsequently, you cannot change the storage type.</span></span>

## <span data-ttu-id="01a51-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="01a51-133">RELATED LINKS</span></span>

[<span data-ttu-id="01a51-134">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="01a51-134">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="01a51-135">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="01a51-135">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="01a51-136">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="01a51-136">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)


