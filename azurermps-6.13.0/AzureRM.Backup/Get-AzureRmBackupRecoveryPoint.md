---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6778E018-B6CC-468A-823E-3DA047EA6B52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
ms.openlocfilehash: f82abc45a9b78093c13764ab0eb28f2593c7fabb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579055"
---
# <span data-ttu-id="3a013-101">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="3a013-101">Get-AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="3a013-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3a013-102">SYNOPSIS</span></span>
<span data-ttu-id="3a013-103">Hämtar återställnings punkterna för ett säkerhetskopierat objekt.</span><span class="sxs-lookup"><span data-stu-id="3a013-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a013-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3a013-104">SYNTAX</span></span>

```
Get-AzureRmBackupRecoveryPoint [[-RecoveryPointId] <String>] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a013-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3a013-105">DESCRIPTION</span></span>
<span data-ttu-id="3a013-106">Cmdleten **Get-AzureRmBackupRecoveryPoint** hämtar återställnings punkterna för ett säkerhetskopierat Azure-säkerhetsobjekt.</span><span class="sxs-lookup"><span data-stu-id="3a013-106">The **Get-AzureRmBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="3a013-107">När ett objekt har säkerhetskopierats lagras en eller flera återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="3a013-107">After an item has been backed up, Backup stores one or more recovery points.</span></span>

## <span data-ttu-id="3a013-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3a013-108">EXAMPLES</span></span>

### <span data-ttu-id="3a013-109">Exempel 1: Hämta återställnings punkter för ett objekt</span><span class="sxs-lookup"><span data-stu-id="3a013-109">Example 1: Get recovery points for an item</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> Get-AzureRmBackupRecoveryPoint -Item $BackupItem
RecoveryPointId    RecoveryPointType  RecoveryPointTime      ContainerName
---------------    -----------------  -----------------      -------------
15273496567119     AppConsistent      26-Aug-15 12:27:38 PM  iaasvmcontainer;conto02-vm;conto0...
```

<span data-ttu-id="3a013-110">Det första kommandot får valvet med namnet Vault03 med hjälp av Get-AzureRmBackupVault cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a013-110">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="3a013-111">Kommandot lagrar objektet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="3a013-111">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="3a013-112">Det andra kommandot får en behållare som har det angivna namnet i valvet i $Vault genom att använda cmdleten **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="3a013-112">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="3a013-113">Kommandot lagrar objektet i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="3a013-113">The command stores that object in the $Container variable.</span></span>
<span data-ttu-id="3a013-114">Det tredje kommandot får säkerhets kopian i behållaren i $Container genom att använda cmdleten **Get-AzureRmBackupItem** .</span><span class="sxs-lookup"><span data-stu-id="3a013-114">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="3a013-115">Kommandot lagrar objektet i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="3a013-115">The command stores that object in the $BackupItem variable.</span></span>
<span data-ttu-id="3a013-116">Det sista kommandot får återställnings punkter för objektet i $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="3a013-116">The final command gets recovery points for the item in $BackupItem.</span></span>

## <span data-ttu-id="3a013-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3a013-117">PARAMETERS</span></span>

### <span data-ttu-id="3a013-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a013-118">-DefaultProfile</span></span>
<span data-ttu-id="3a013-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3a013-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a013-120">-Objekt</span><span class="sxs-lookup"><span data-stu-id="3a013-120">-Item</span></span>
<span data-ttu-id="3a013-121">Anger objekt för vilka denna cmdlet hämtar återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="3a013-121">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="3a013-122">För att få en **AzureRmBackupItem** , Använd cmdleten Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="3a013-122">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a013-123">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="3a013-123">-RecoveryPointId</span></span>
<span data-ttu-id="3a013-124">Anger ID för en återställnings punkt som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="3a013-124">Specifies the ID of a recovery point that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a013-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a013-125">CommonParameters</span></span>
<span data-ttu-id="3a013-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a013-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a013-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a013-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a013-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3a013-128">INPUTS</span></span>

### <span data-ttu-id="3a013-129">Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="3a013-129">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem</span></span>
<span data-ttu-id="3a013-130">Parametrar: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3a013-130">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="3a013-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3a013-131">OUTPUTS</span></span>

### <span data-ttu-id="3a013-132">Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="3a013-132">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRecoveryPoint</span></span>

## <span data-ttu-id="3a013-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3a013-133">NOTES</span></span>

## <span data-ttu-id="3a013-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3a013-134">RELATED LINKS</span></span>

[<span data-ttu-id="3a013-135">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="3a013-135">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="3a013-136">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="3a013-136">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="3a013-137">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="3a013-137">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


