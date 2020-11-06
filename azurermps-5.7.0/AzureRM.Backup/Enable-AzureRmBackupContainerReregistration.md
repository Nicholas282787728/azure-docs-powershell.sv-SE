---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 2605B232-10CA-4426-9917-7C9719C15166
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupcontainerreregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
ms.openlocfilehash: f64453995418df572480426e7c2c63e497cf000f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582100"
---
# <span data-ttu-id="447ec-101">Enable-AzureRmBackupContainerReregistration</span><span class="sxs-lookup"><span data-stu-id="447ec-101">Enable-AzureRmBackupContainerReregistration</span></span>

## <span data-ttu-id="447ec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="447ec-102">SYNOPSIS</span></span>
<span data-ttu-id="447ec-103">Registrerar en server för att ansluta till ett säkerhets kopierings valv.</span><span class="sxs-lookup"><span data-stu-id="447ec-103">Reregisters a server to connect to a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="447ec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="447ec-104">SYNTAX</span></span>

```
Enable-AzureRmBackupContainerReregistration [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="447ec-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="447ec-105">DESCRIPTION</span></span>
<span data-ttu-id="447ec-106">Cmdleten **Enable-AzureRmBackupContainerReregistration** registrerar en server för att ansluta till ett Azure Backup-valv och fortsätter med plats kedjan för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="447ec-106">The **Enable-AzureRmBackupContainerReregistration** cmdlet reregisters a server to connect to an Azure Backup vault and continue the Backup recovery point chain.</span></span>

<span data-ttu-id="447ec-107">Om du förstör en server kvarstår alla dess säkerhets kopierings punkter i säkerhets kopierings valvet.</span><span class="sxs-lookup"><span data-stu-id="447ec-107">If you destroy a server, all its cloud backup points remain in the Backup vault.</span></span>
<span data-ttu-id="447ec-108">Om du skapar en ersättnings Server och tilldelar den samma fullkvalificerade domän namn kan du koppla tillbaka servern till samma valv.</span><span class="sxs-lookup"><span data-stu-id="447ec-108">If you create a replacement server and assign it the same fully qualified domain name, you can connect the server back to the same vault.</span></span>
<span data-ttu-id="447ec-109">Med den här cmdleten kan du göra säkerhets kopior och lägga till nya säkerhets kopior i den befintliga uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="447ec-109">This cmdlet enables Backup to make backups and add new backup points to the existing set.</span></span>
<span data-ttu-id="447ec-110">Den nya servern fortsätter i säkerhets kopierings kedjan.</span><span class="sxs-lookup"><span data-stu-id="447ec-110">The new the server continues in the backup chain.</span></span>

## <span data-ttu-id="447ec-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="447ec-111">EXAMPLES</span></span>

## <span data-ttu-id="447ec-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="447ec-112">PARAMETERS</span></span>

### <span data-ttu-id="447ec-113">-Container</span><span class="sxs-lookup"><span data-stu-id="447ec-113">-Container</span></span>
<span data-ttu-id="447ec-114">Anger den behållare som den här cmdleten registrerar.</span><span class="sxs-lookup"><span data-stu-id="447ec-114">Specifies the container that this cmdlet reregisters.</span></span>
<span data-ttu-id="447ec-115">För att få en **AzureRmBackupContainer** , Använd cmdleten Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="447ec-115">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="447ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="447ec-116">-DefaultProfile</span></span>
<span data-ttu-id="447ec-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="447ec-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="447ec-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="447ec-118">CommonParameters</span></span>
<span data-ttu-id="447ec-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="447ec-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="447ec-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="447ec-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="447ec-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="447ec-121">INPUTS</span></span>

### <span data-ttu-id="447ec-122">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="447ec-122">AzureBackupContainer</span></span>

## <span data-ttu-id="447ec-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="447ec-123">OUTPUTS</span></span>

### <span data-ttu-id="447ec-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="447ec-124">None</span></span>

## <span data-ttu-id="447ec-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="447ec-125">NOTES</span></span>

## <span data-ttu-id="447ec-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="447ec-126">RELATED LINKS</span></span>

[<span data-ttu-id="447ec-127">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="447ec-127">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="447ec-128">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="447ec-128">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)


