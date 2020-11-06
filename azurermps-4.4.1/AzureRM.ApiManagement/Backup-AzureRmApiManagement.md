---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
ms.openlocfilehash: d036b31f521736420b91b04b4f6f5513f3dbc50d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581563"
---
# <span data-ttu-id="e01f3-101">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e01f3-101">Backup-AzureRmApiManagement</span></span>

## <span data-ttu-id="e01f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e01f3-102">SYNOPSIS</span></span>
<span data-ttu-id="e01f3-103">Säkerhetskopierar en API-hanterings tjänst.</span><span class="sxs-lookup"><span data-stu-id="e01f3-103">Backs up an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e01f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e01f3-104">SYNTAX</span></span>

```
Backup-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e01f3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e01f3-105">DESCRIPTION</span></span>
<span data-ttu-id="e01f3-106">**Säkerhets kopiering-AzureRmApiManagement** cmdlet säkerhetskopierar en instans av en Azure API Management-tjänst.</span><span class="sxs-lookup"><span data-stu-id="e01f3-106">The **Backup-AzureRmApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="e01f3-107">Denna cmdlet lagrar säkerhets kopian som en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="e01f3-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="e01f3-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e01f3-108">EXAMPLES</span></span>

### <span data-ttu-id="e01f3-109">Exempel 1: säkerhetskopiera en API-hanterings tjänst</span><span class="sxs-lookup"><span data-stu-id="e01f3-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>Backup-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="e01f3-110">Det här kommandot säkerhetskopierar en API-hanterings tjänst till en lagrings-blob.</span><span class="sxs-lookup"><span data-stu-id="e01f3-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="e01f3-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e01f3-111">PARAMETERS</span></span>

### <span data-ttu-id="e01f3-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="e01f3-112">-Name</span></span>
<span data-ttu-id="e01f3-113">Anger namnet på den API-hanterings distribution som denna cmdlet säkerhetskopierar.</span><span class="sxs-lookup"><span data-stu-id="e01f3-113">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="e01f3-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e01f3-114">-PassThru</span></span>
<span data-ttu-id="e01f3-115">Anger att den här cmdleten returnerar det säkerhetskopierade **PsApiManagement** -objektet, om åtgärden lyckas.</span><span class="sxs-lookup"><span data-stu-id="e01f3-115">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="e01f3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e01f3-116">-ResourceGroupName</span></span>
<span data-ttu-id="e01f3-117">Anger namnet på den resurs grupp som distributionen av API-hanteringen finns under.</span><span class="sxs-lookup"><span data-stu-id="e01f3-117">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="e01f3-118">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="e01f3-118">-StorageContext</span></span>
<span data-ttu-id="e01f3-119">Anger en kontext för lagrings anslutning.</span><span class="sxs-lookup"><span data-stu-id="e01f3-119">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="e01f3-120">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="e01f3-120">-TargetBlobName</span></span>
<span data-ttu-id="e01f3-121">Anger namnet på blobben för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="e01f3-121">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="e01f3-122">Om blobben inte finns skapar den här cmdlet den.</span><span class="sxs-lookup"><span data-stu-id="e01f3-122">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="e01f3-123">Denna cmdlet skapar ett standardvärde baserat på följande mönster:</span><span class="sxs-lookup"><span data-stu-id="e01f3-123">This cmdlet generates a default value based on the following pattern:</span></span> 

<span data-ttu-id="e01f3-124">{Name}-{ÅÅÅÅ-MM-dd-HH-mm}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="e01f3-124">{Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="e01f3-125">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="e01f3-125">-TargetContainerName</span></span>
<span data-ttu-id="e01f3-126">Anger namnet på behållaren för blobben för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="e01f3-126">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="e01f3-127">Om behållaren inte finns skapar den här cmdlet den.</span><span class="sxs-lookup"><span data-stu-id="e01f3-127">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="e01f3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e01f3-128">-DefaultProfile</span></span>
<span data-ttu-id="e01f3-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e01f3-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e01f3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e01f3-130">CommonParameters</span></span>
<span data-ttu-id="e01f3-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e01f3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e01f3-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e01f3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e01f3-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e01f3-133">INPUTS</span></span>

## <span data-ttu-id="e01f3-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e01f3-134">OUTPUTS</span></span>

### <span data-ttu-id="e01f3-135">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e01f3-135">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="e01f3-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e01f3-136">NOTES</span></span>

## <span data-ttu-id="e01f3-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e01f3-137">RELATED LINKS</span></span>

[<span data-ttu-id="e01f3-138">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e01f3-138">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="e01f3-139">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e01f3-139">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="e01f3-140">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e01f3-140">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="e01f3-141">Återställ-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e01f3-141">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


