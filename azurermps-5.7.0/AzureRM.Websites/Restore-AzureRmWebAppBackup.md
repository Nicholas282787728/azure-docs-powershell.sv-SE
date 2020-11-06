---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: c68d9afb7c9498bbf734abcc376e6f123ebb8ac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581864"
---
# <span data-ttu-id="481ed-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="481ed-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="481ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="481ed-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="481ed-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="481ed-103">SYNTAX</span></span>

### <span data-ttu-id="481ed-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="481ed-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

### <span data-ttu-id="481ed-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="481ed-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String>
 [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="481ed-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="481ed-106">DESCRIPTION</span></span>
<span data-ttu-id="481ed-107">Cmdleten **restore-AzureRmWebAppBackup** återställer en Azure Web App-säkerhetskopia.</span><span class="sxs-lookup"><span data-stu-id="481ed-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="481ed-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="481ed-108">EXAMPLES</span></span>

### <span data-ttu-id="481ed-109">9.1</span><span class="sxs-lookup"><span data-stu-id="481ed-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="481ed-110">Återställer en säkerhets kopia av den angivna app-ContosoWebApp som ingår i resurs gruppens standardinställning-väst i BLOB "mittArkiv" på https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="481ed-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="481ed-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="481ed-111">PARAMETERS</span></span>

### <span data-ttu-id="481ed-112">-BlobName</span><span class="sxs-lookup"><span data-stu-id="481ed-112">-BlobName</span></span>
<span data-ttu-id="481ed-113">BLOB-namn</span><span class="sxs-lookup"><span data-stu-id="481ed-113">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="481ed-114">-Databaser</span><span class="sxs-lookup"><span data-stu-id="481ed-114">-Databases</span></span>
<span data-ttu-id="481ed-115">Databaser av typen DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="481ed-115">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="481ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="481ed-116">-DefaultProfile</span></span>
<span data-ttu-id="481ed-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="481ed-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="481ed-118">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="481ed-118">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="481ed-119">Ignorera alternativ för värdbaserade namn</span><span class="sxs-lookup"><span data-stu-id="481ed-119">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="481ed-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="481ed-120">-Name</span></span>
<span data-ttu-id="481ed-121">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="481ed-121">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="481ed-122">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="481ed-122">-Overwrite</span></span>
<span data-ttu-id="481ed-123">Alternativet överskrivning</span><span class="sxs-lookup"><span data-stu-id="481ed-123">Overwrite Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="481ed-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="481ed-124">-ResourceGroupName</span></span>
<span data-ttu-id="481ed-125">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="481ed-125">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="481ed-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="481ed-126">-Slot</span></span>
<span data-ttu-id="481ed-127">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="481ed-127">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="481ed-128">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="481ed-128">-StorageAccountUrl</span></span>
<span data-ttu-id="481ed-129">URL för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="481ed-129">Storage Account Url</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="481ed-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="481ed-130">-WebApp</span></span>
<span data-ttu-id="481ed-131">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="481ed-131">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="481ed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="481ed-132">CommonParameters</span></span>
<span data-ttu-id="481ed-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="481ed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="481ed-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="481ed-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="481ed-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="481ed-135">INPUTS</span></span>

### <span data-ttu-id="481ed-136">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="481ed-136">Site</span></span>
<span data-ttu-id="481ed-137">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="481ed-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="481ed-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="481ed-138">OUTPUTS</span></span>

## <span data-ttu-id="481ed-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="481ed-139">NOTES</span></span>

## <span data-ttu-id="481ed-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="481ed-140">RELATED LINKS</span></span>

