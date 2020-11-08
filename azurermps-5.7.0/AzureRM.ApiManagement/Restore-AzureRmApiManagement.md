---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/restore-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
ms.openlocfilehash: 3de18d5d7cc1c3525f1526beb5dd7337175eb041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758353"
---
# <span data-ttu-id="0af87-101">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0af87-101">Restore-AzureRmApiManagement</span></span>

## <span data-ttu-id="0af87-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0af87-102">SYNOPSIS</span></span>
<span data-ttu-id="0af87-103">Återställer en API-hanterings tjänst från den angivna Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="0af87-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0af87-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0af87-104">SYNTAX</span></span>

```
Restore-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0af87-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0af87-105">DESCRIPTION</span></span>
<span data-ttu-id="0af87-106">Cmdleten **restore-AzureRmApiManagement** återställer en API-hanterings tjänst från den angivna säkerhets kopian i en Azurestorage-blob.</span><span class="sxs-lookup"><span data-stu-id="0af87-106">The **Restore-AzureRmApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="0af87-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0af87-107">EXAMPLES</span></span>

### <span data-ttu-id="0af87-108">Exempel 1: återställa en API-hanterings tjänst</span><span class="sxs-lookup"><span data-stu-id="0af87-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzureRmStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzureRmStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzureStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="0af87-109">Det här kommandot återställer en API-hanterings tjänst från Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="0af87-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="0af87-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0af87-110">PARAMETERS</span></span>

### <span data-ttu-id="0af87-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af87-111">-DefaultProfile</span></span>
<span data-ttu-id="0af87-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0af87-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="0af87-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="0af87-113">-Name</span></span>
<span data-ttu-id="0af87-114">Anger namnet på API-hanteringskonsolen som kommer att återställas med säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="0af87-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="0af87-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0af87-115">-PassThru</span></span>
<span data-ttu-id="0af87-116">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="0af87-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0af87-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="0af87-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0af87-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0af87-118">-ResourceGroupName</span></span>
<span data-ttu-id="0af87-119">Anger namnet på den resurs grupp som API-hantering finns under.</span><span class="sxs-lookup"><span data-stu-id="0af87-119">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="0af87-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="0af87-120">-SourceBlobName</span></span>
<span data-ttu-id="0af87-121">Anger namnet på käll-BLOB för Azure Storage backup.</span><span class="sxs-lookup"><span data-stu-id="0af87-121">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="0af87-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="0af87-122">-SourceContainerName</span></span>
<span data-ttu-id="0af87-123">Anger namnet på käll behållaren för en Azure Storage-säkerhetskopiering.</span><span class="sxs-lookup"><span data-stu-id="0af87-123">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="0af87-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="0af87-124">-StorageContext</span></span>
<span data-ttu-id="0af87-125">Anger kontext för lagrings anslutning.</span><span class="sxs-lookup"><span data-stu-id="0af87-125">Specifies the storage connection context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af87-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af87-126">CommonParameters</span></span>
<span data-ttu-id="0af87-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0af87-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af87-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0af87-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af87-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0af87-129">INPUTS</span></span>

### <span data-ttu-id="0af87-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="0af87-130">None</span></span>
<span data-ttu-id="0af87-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="0af87-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0af87-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0af87-132">OUTPUTS</span></span>

### <span data-ttu-id="0af87-133">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="0af87-133">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="0af87-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0af87-134">NOTES</span></span>

## <span data-ttu-id="0af87-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0af87-135">RELATED LINKS</span></span>

[<span data-ttu-id="0af87-136">Säkerhets kopiering-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0af87-136">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="0af87-137">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0af87-137">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="0af87-138">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0af87-138">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="0af87-139">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0af87-139">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

