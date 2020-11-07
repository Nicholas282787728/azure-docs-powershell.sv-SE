---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/backup-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
ms.openlocfilehash: 0fd004cdb727a0e665fd9b867854b3b8e4054c9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758362"
---
# <span data-ttu-id="03639-101">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="03639-101">Backup-AzureRmApiManagement</span></span>

## <span data-ttu-id="03639-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03639-102">SYNOPSIS</span></span>
<span data-ttu-id="03639-103">Säkerhetskopierar en API-hanterings tjänst.</span><span class="sxs-lookup"><span data-stu-id="03639-103">Backs up an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03639-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03639-104">SYNTAX</span></span>

```
Backup-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03639-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03639-105">DESCRIPTION</span></span>
<span data-ttu-id="03639-106">**Säkerhets kopiering-AzureRmApiManagement** cmdlet säkerhetskopierar en instans av en Azure API Management-tjänst.</span><span class="sxs-lookup"><span data-stu-id="03639-106">The **Backup-AzureRmApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="03639-107">Denna cmdlet lagrar säkerhets kopian som en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="03639-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="03639-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03639-108">EXAMPLES</span></span>

### <span data-ttu-id="03639-109">Exempel 1: säkerhetskopiera en API-hanterings tjänst</span><span class="sxs-lookup"><span data-stu-id="03639-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzureRmStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzureRmStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzureStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="03639-110">Det här kommandot säkerhetskopierar en API-hanterings tjänst till en lagrings-blob.</span><span class="sxs-lookup"><span data-stu-id="03639-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="03639-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03639-111">PARAMETERS</span></span>

### <span data-ttu-id="03639-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03639-112">-DefaultProfile</span></span>
<span data-ttu-id="03639-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="03639-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="03639-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="03639-114">-Name</span></span>
<span data-ttu-id="03639-115">Anger namnet på den API-hanterings distribution som denna cmdlet säkerhetskopierar.</span><span class="sxs-lookup"><span data-stu-id="03639-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03639-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03639-116">-PassThru</span></span>
<span data-ttu-id="03639-117">Anger att den här cmdleten returnerar det säkerhetskopierade **PsApiManagement** -objektet, om åtgärden lyckas.</span><span class="sxs-lookup"><span data-stu-id="03639-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03639-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03639-118">-ResourceGroupName</span></span>
<span data-ttu-id="03639-119">Anger namnet på den resurs grupp som distributionen av API-hanteringen finns under.</span><span class="sxs-lookup"><span data-stu-id="03639-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03639-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="03639-120">-StorageContext</span></span>
<span data-ttu-id="03639-121">Anger en kontext för lagrings anslutning.</span><span class="sxs-lookup"><span data-stu-id="03639-121">Specifies a storage connection context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03639-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="03639-122">-TargetBlobName</span></span>
<span data-ttu-id="03639-123">Anger namnet på blobben för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="03639-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="03639-124">Om blobben inte finns skapar den här cmdlet den.</span><span class="sxs-lookup"><span data-stu-id="03639-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="03639-125">Denna cmdlet skapar ett standardvärde baserat på följande mönster:</span><span class="sxs-lookup"><span data-stu-id="03639-125">This cmdlet generates a default value based on the following pattern:</span></span> 

<span data-ttu-id="03639-126">{Name}-{ÅÅÅÅ-MM-dd-HH-mm}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="03639-126">{Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03639-127">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="03639-127">-TargetContainerName</span></span>
<span data-ttu-id="03639-128">Anger namnet på behållaren för blobben för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="03639-128">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="03639-129">Om behållaren inte finns skapar den här cmdlet den.</span><span class="sxs-lookup"><span data-stu-id="03639-129">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="03639-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03639-130">CommonParameters</span></span>
<span data-ttu-id="03639-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03639-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03639-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03639-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03639-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03639-133">INPUTS</span></span>

### <span data-ttu-id="03639-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="03639-134">None</span></span>
<span data-ttu-id="03639-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="03639-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="03639-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03639-136">OUTPUTS</span></span>

### <span data-ttu-id="03639-137">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="03639-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="03639-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03639-138">NOTES</span></span>

## <span data-ttu-id="03639-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03639-139">RELATED LINKS</span></span>

[<span data-ttu-id="03639-140">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="03639-140">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="03639-141">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="03639-141">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="03639-142">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="03639-142">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="03639-143">Återställ-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="03639-143">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


