---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/backup-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
ms.openlocfilehash: d8f243b0b02d724a3979b8c8f318be8e58623cf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581839"
---
# <span data-ttu-id="df6d2-101">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="df6d2-101">Backup-AzureRmApiManagement</span></span>

## <span data-ttu-id="df6d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df6d2-102">SYNOPSIS</span></span>
<span data-ttu-id="df6d2-103">Säkerhetskopierar en API-hanterings tjänst.</span><span class="sxs-lookup"><span data-stu-id="df6d2-103">Backs up an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df6d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df6d2-104">SYNTAX</span></span>

```
Backup-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df6d2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df6d2-105">DESCRIPTION</span></span>
<span data-ttu-id="df6d2-106">**Säkerhets kopiering-AzureRmApiManagement** cmdlet säkerhetskopierar en instans av en Azure API Management-tjänst.</span><span class="sxs-lookup"><span data-stu-id="df6d2-106">The **Backup-AzureRmApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="df6d2-107">Denna cmdlet lagrar säkerhets kopian som en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="df6d2-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="df6d2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df6d2-108">EXAMPLES</span></span>

### <span data-ttu-id="df6d2-109">Exempel 1: säkerhetskopiera en API-hanterings tjänst</span><span class="sxs-lookup"><span data-stu-id="df6d2-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzureRmStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzureRmStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzureStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="df6d2-110">Det här kommandot säkerhetskopierar en API-hanterings tjänst till en lagrings-blob.</span><span class="sxs-lookup"><span data-stu-id="df6d2-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="df6d2-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df6d2-111">PARAMETERS</span></span>

### <span data-ttu-id="df6d2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df6d2-112">-DefaultProfile</span></span>
<span data-ttu-id="df6d2-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df6d2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df6d2-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="df6d2-114">-Name</span></span>
<span data-ttu-id="df6d2-115">Anger namnet på den API-hanterings distribution som denna cmdlet säkerhetskopierar.</span><span class="sxs-lookup"><span data-stu-id="df6d2-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6d2-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df6d2-116">-PassThru</span></span>
<span data-ttu-id="df6d2-117">Anger att den här cmdleten returnerar det säkerhetskopierade **PsApiManagement** -objektet, om åtgärden lyckas.</span><span class="sxs-lookup"><span data-stu-id="df6d2-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df6d2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df6d2-118">-ResourceGroupName</span></span>
<span data-ttu-id="df6d2-119">Anger namnet på den resurs grupp som distributionen av API-hanteringen finns under.</span><span class="sxs-lookup"><span data-stu-id="df6d2-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6d2-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="df6d2-120">-StorageContext</span></span>
<span data-ttu-id="df6d2-121">Anger en kontext för lagrings anslutning.</span><span class="sxs-lookup"><span data-stu-id="df6d2-121">Specifies a storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6d2-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="df6d2-122">-TargetBlobName</span></span>
<span data-ttu-id="df6d2-123">Anger namnet på blobben för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="df6d2-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="df6d2-124">Om blobben inte finns skapar den här cmdlet den.</span><span class="sxs-lookup"><span data-stu-id="df6d2-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="df6d2-125">Denna cmdlet genererar ett standardvärde baserat på följande mönster: {Name}-{ÅÅÅÅ-MM-dd-HH-mm}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="df6d2-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df6d2-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="df6d2-126">-TargetContainerName</span></span>
<span data-ttu-id="df6d2-127">Anger namnet på behållaren för blobben för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="df6d2-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="df6d2-128">Om behållaren inte finns skapar den här cmdlet den.</span><span class="sxs-lookup"><span data-stu-id="df6d2-128">If the container does not exist, this cmdlet creates it.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df6d2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df6d2-129">CommonParameters</span></span>
<span data-ttu-id="df6d2-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df6d2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df6d2-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df6d2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df6d2-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df6d2-132">INPUTS</span></span>

### <span data-ttu-id="df6d2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="df6d2-133">System.String</span></span>

### <span data-ttu-id="df6d2-134">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="df6d2-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="df6d2-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df6d2-135">OUTPUTS</span></span>

### <span data-ttu-id="df6d2-136">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="df6d2-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="df6d2-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df6d2-137">NOTES</span></span>

## <span data-ttu-id="df6d2-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df6d2-138">RELATED LINKS</span></span>

[<span data-ttu-id="df6d2-139">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="df6d2-139">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="df6d2-140">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="df6d2-140">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="df6d2-141">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="df6d2-141">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="df6d2-142">Återställ-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="df6d2-142">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


