---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: d99db4c9fe2c69e2177d9b35e15b49957e910014
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261473"
---
# <span data-ttu-id="dd8ea-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd8ea-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="dd8ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dd8ea-102">SYNOPSIS</span></span>
<span data-ttu-id="dd8ea-103">Återställer en API-hanterings tjänst från den angivna Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="dd8ea-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="dd8ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dd8ea-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd8ea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dd8ea-105">DESCRIPTION</span></span>
<span data-ttu-id="dd8ea-106">Cmdleten **restore-AzApiManagement** återställer en API-hanterings tjänst från den angivna säkerhets kopian i en Azurestorage-blob.</span><span class="sxs-lookup"><span data-stu-id="dd8ea-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="dd8ea-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dd8ea-107">EXAMPLES</span></span>

### <span data-ttu-id="dd8ea-108">Exempel 1: återställa en API-hanterings tjänst</span><span class="sxs-lookup"><span data-stu-id="dd8ea-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="dd8ea-109">Det här kommandot återställer en API-hanterings tjänst från Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="dd8ea-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="dd8ea-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dd8ea-110">PARAMETERS</span></span>

### <span data-ttu-id="dd8ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd8ea-111">-DefaultProfile</span></span>
<span data-ttu-id="dd8ea-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dd8ea-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd8ea-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="dd8ea-113">-Name</span></span>
<span data-ttu-id="dd8ea-114">Anger namnet på API-hanteringskonsolen som kommer att återställas med säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="dd8ea-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="dd8ea-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd8ea-115">-PassThru</span></span>
<span data-ttu-id="dd8ea-116">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="dd8ea-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dd8ea-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="dd8ea-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dd8ea-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd8ea-118">-ResourceGroupName</span></span>
<span data-ttu-id="dd8ea-119">Anger namnet på den resurs grupp som API-hantering finns under.</span><span class="sxs-lookup"><span data-stu-id="dd8ea-119">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="dd8ea-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="dd8ea-120">-SourceBlobName</span></span>
<span data-ttu-id="dd8ea-121">Anger namnet på käll-BLOB för Azure Storage backup.</span><span class="sxs-lookup"><span data-stu-id="dd8ea-121">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="dd8ea-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="dd8ea-122">-SourceContainerName</span></span>
<span data-ttu-id="dd8ea-123">Anger namnet på käll behållaren för en Azure Storage-säkerhetskopiering.</span><span class="sxs-lookup"><span data-stu-id="dd8ea-123">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="dd8ea-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="dd8ea-124">-StorageContext</span></span>
<span data-ttu-id="dd8ea-125">Anger kontext för lagrings anslutning.</span><span class="sxs-lookup"><span data-stu-id="dd8ea-125">Specifies the storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8ea-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd8ea-126">CommonParameters</span></span>
<span data-ttu-id="dd8ea-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd8ea-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd8ea-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd8ea-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd8ea-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dd8ea-129">INPUTS</span></span>

### <span data-ttu-id="dd8ea-130">System. String</span><span class="sxs-lookup"><span data-stu-id="dd8ea-130">System.String</span></span>

## <span data-ttu-id="dd8ea-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dd8ea-131">OUTPUTS</span></span>

### <span data-ttu-id="dd8ea-132">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd8ea-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="dd8ea-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dd8ea-133">NOTES</span></span>

## <span data-ttu-id="dd8ea-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dd8ea-134">RELATED LINKS</span></span>

[<span data-ttu-id="dd8ea-135">Säkerhets kopiering-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd8ea-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="dd8ea-136">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd8ea-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="dd8ea-137">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd8ea-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="dd8ea-138">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd8ea-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)


