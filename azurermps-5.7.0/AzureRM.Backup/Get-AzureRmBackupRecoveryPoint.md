---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6778E018-B6CC-468A-823E-3DA047EA6B52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
ms.openlocfilehash: 2805ebfd5849306dadb4cf913660c8fac1602d79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578343"
---
# <span data-ttu-id="a2438-101">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a2438-101">Get-AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="a2438-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2438-102">SYNOPSIS</span></span>
<span data-ttu-id="a2438-103">Hämtar återställnings punkterna för ett säkerhetskopierat objekt.</span><span class="sxs-lookup"><span data-stu-id="a2438-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2438-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2438-104">SYNTAX</span></span>

```
Get-AzureRmBackupRecoveryPoint [[-RecoveryPointId] <String>] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2438-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2438-105">DESCRIPTION</span></span>
<span data-ttu-id="a2438-106">Cmdleten **Get-AzureRmBackupRecoveryPoint** hämtar återställnings punkterna för ett säkerhetskopierat Azure-säkerhetsobjekt.</span><span class="sxs-lookup"><span data-stu-id="a2438-106">The **Get-AzureRmBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="a2438-107">När ett objekt har säkerhetskopierats lagras en eller flera återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="a2438-107">After an item has been backed up, Backup stores one or more recovery points.</span></span>

## <span data-ttu-id="a2438-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2438-108">EXAMPLES</span></span>

### <span data-ttu-id="a2438-109">Exempel 1: Hämta återställnings punkter för ett objekt</span><span class="sxs-lookup"><span data-stu-id="a2438-109">Example 1: Get recovery points for an item</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> Get-AzureRmBackupRecoveryPoint -Item $BackupItem
RecoveryPointId    RecoveryPointType  RecoveryPointTime      ContainerName
---------------    -----------------  -----------------      -------------
15273496567119     AppConsistent      26-Aug-15 12:27:38 PM  iaasvmcontainer;conto02-vm;conto0...
```

<span data-ttu-id="a2438-110">Det första kommandot får valvet med namnet Vault03 med hjälp av Get-AzureRmBackupVault cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2438-110">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="a2438-111">Kommandot lagrar objektet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="a2438-111">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="a2438-112">Det andra kommandot får en behållare som har det angivna namnet i valvet i $Vault genom att använda cmdleten **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="a2438-112">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="a2438-113">Kommandot lagrar objektet i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="a2438-113">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="a2438-114">Det tredje kommandot får säkerhets kopian i behållaren i $Container genom att använda cmdleten **Get-AzureRmBackupItem** .</span><span class="sxs-lookup"><span data-stu-id="a2438-114">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="a2438-115">Kommandot lagrar objektet i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="a2438-115">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="a2438-116">Det sista kommandot får återställnings punkter för objektet i $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="a2438-116">The final command gets recovery points for the item in $BackupItem.</span></span>

## <span data-ttu-id="a2438-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2438-117">PARAMETERS</span></span>

### <span data-ttu-id="a2438-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2438-118">-DefaultProfile</span></span>
<span data-ttu-id="a2438-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a2438-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2438-120">-Objekt</span><span class="sxs-lookup"><span data-stu-id="a2438-120">-Item</span></span>
<span data-ttu-id="a2438-121">Anger objekt för vilka denna cmdlet hämtar återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="a2438-121">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="a2438-122">För att få en **AzureRmBackupItem** , Använd cmdleten Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="a2438-122">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2438-123">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="a2438-123">-RecoveryPointId</span></span>
<span data-ttu-id="a2438-124">Anger ID för en återställnings punkt som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="a2438-124">Specifies the ID of a recovery point that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2438-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2438-125">CommonParameters</span></span>
<span data-ttu-id="a2438-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2438-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2438-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2438-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2438-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2438-128">INPUTS</span></span>

### <span data-ttu-id="a2438-129">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="a2438-129">AzureRmBackupItem</span></span>

## <span data-ttu-id="a2438-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2438-130">OUTPUTS</span></span>

### <span data-ttu-id="a2438-131">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a2438-131">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="a2438-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2438-132">NOTES</span></span>

## <span data-ttu-id="a2438-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2438-133">RELATED LINKS</span></span>

[<span data-ttu-id="a2438-134">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="a2438-134">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="a2438-135">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="a2438-135">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="a2438-136">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="a2438-136">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


