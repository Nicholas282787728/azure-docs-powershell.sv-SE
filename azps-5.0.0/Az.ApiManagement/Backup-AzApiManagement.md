---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: fcdd498c99c10857e0fa76c890bc6be6e9733b84
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321964"
---
# <span data-ttu-id="8b749-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="8b749-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="8b749-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b749-102">SYNOPSIS</span></span>
<span data-ttu-id="8b749-103">Säkerhetskopierar en API-hanterings tjänst.</span><span class="sxs-lookup"><span data-stu-id="8b749-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="8b749-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b749-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b749-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b749-105">DESCRIPTION</span></span>
<span data-ttu-id="8b749-106">**Säkerhets kopiering-AzApiManagement** cmdlet säkerhetskopierar en instans av en Azure API Management-tjänst.</span><span class="sxs-lookup"><span data-stu-id="8b749-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="8b749-107">Denna cmdlet lagrar säkerhets kopian som en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="8b749-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="8b749-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b749-108">EXAMPLES</span></span>

### <span data-ttu-id="8b749-109">Exempel 1: säkerhetskopiera en API-hanterings tjänst</span><span class="sxs-lookup"><span data-stu-id="8b749-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="8b749-110">Det här kommandot säkerhetskopierar en API-hanterings tjänst till en lagrings-blob.</span><span class="sxs-lookup"><span data-stu-id="8b749-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="8b749-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b749-111">PARAMETERS</span></span>

### <span data-ttu-id="8b749-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b749-112">-DefaultProfile</span></span>
<span data-ttu-id="8b749-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8b749-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b749-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="8b749-114">-Name</span></span>
<span data-ttu-id="8b749-115">Anger namnet på den API-hanterings distribution som denna cmdlet säkerhetskopierar.</span><span class="sxs-lookup"><span data-stu-id="8b749-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="8b749-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b749-116">-PassThru</span></span>
<span data-ttu-id="8b749-117">Anger att den här cmdleten returnerar det säkerhetskopierade **PsApiManagement** -objektet, om åtgärden lyckas.</span><span class="sxs-lookup"><span data-stu-id="8b749-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="8b749-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b749-118">-ResourceGroupName</span></span>
<span data-ttu-id="8b749-119">Anger namnet på den resurs grupp som distributionen av API-hanteringen finns under.</span><span class="sxs-lookup"><span data-stu-id="8b749-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="8b749-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="8b749-120">-StorageContext</span></span>
<span data-ttu-id="8b749-121">Anger en kontext för lagrings anslutning.</span><span class="sxs-lookup"><span data-stu-id="8b749-121">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="8b749-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="8b749-122">-TargetBlobName</span></span>
<span data-ttu-id="8b749-123">Anger namnet på blobben för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="8b749-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="8b749-124">Om blobben inte finns skapar den här cmdlet den.</span><span class="sxs-lookup"><span data-stu-id="8b749-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="8b749-125">Denna cmdlet genererar ett standardvärde baserat på följande mönster: {Name}-{ÅÅÅÅ-MM-dd-HH-mm}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="8b749-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="8b749-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="8b749-126">-TargetContainerName</span></span>
<span data-ttu-id="8b749-127">Anger namnet på behållaren för blobben för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="8b749-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="8b749-128">Om behållaren inte finns skapar den här cmdlet den.</span><span class="sxs-lookup"><span data-stu-id="8b749-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="8b749-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b749-129">CommonParameters</span></span>
<span data-ttu-id="8b749-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b749-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b749-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b749-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b749-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b749-132">INPUTS</span></span>

### <span data-ttu-id="8b749-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8b749-133">System.String</span></span>

### <span data-ttu-id="8b749-134">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8b749-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8b749-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b749-135">OUTPUTS</span></span>

### <span data-ttu-id="8b749-136">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="8b749-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="8b749-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b749-137">NOTES</span></span>

## <span data-ttu-id="8b749-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b749-138">RELATED LINKS</span></span>

[<span data-ttu-id="8b749-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="8b749-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="8b749-140">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="8b749-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="8b749-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="8b749-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="8b749-142">Återställ-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="8b749-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


