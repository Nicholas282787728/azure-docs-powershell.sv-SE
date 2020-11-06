---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: 07cf4daffeaf00c516bc5b179e5f4a2133a2c4ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573601"
---
# <span data-ttu-id="a8ae6-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="a8ae6-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="a8ae6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8ae6-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8ae6-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8ae6-103">SYNTAX</span></span>

### <span data-ttu-id="a8ae6-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="a8ae6-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

### <span data-ttu-id="a8ae6-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="a8ae6-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String>
 [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="a8ae6-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8ae6-106">DESCRIPTION</span></span>
<span data-ttu-id="a8ae6-107">Cmdleten **restore-AzureRmWebAppBackup** återställer en Azure Web App-säkerhetskopia.</span><span class="sxs-lookup"><span data-stu-id="a8ae6-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="a8ae6-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8ae6-108">EXAMPLES</span></span>

### <span data-ttu-id="a8ae6-109">9.1</span><span class="sxs-lookup"><span data-stu-id="a8ae6-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="a8ae6-110">Återställer en säkerhets kopia av den angivna app-ContosoWebApp som ingår i resurs gruppens standardinställning-väst i BLOB "mittArkiv" på https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="a8ae6-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="a8ae6-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8ae6-111">PARAMETERS</span></span>

### <span data-ttu-id="a8ae6-112">-BlobName</span><span class="sxs-lookup"><span data-stu-id="a8ae6-112">-BlobName</span></span>
<span data-ttu-id="a8ae6-113">BLOB-namn</span><span class="sxs-lookup"><span data-stu-id="a8ae6-113">Blob Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ae6-114">-Databaser</span><span class="sxs-lookup"><span data-stu-id="a8ae6-114">-Databases</span></span>
<span data-ttu-id="a8ae6-115">Databaser av typen DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="a8ae6-115">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ae6-116">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="a8ae6-116">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="a8ae6-117">Ignorera alternativ för värdbaserade namn</span><span class="sxs-lookup"><span data-stu-id="a8ae6-117">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ae6-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="a8ae6-118">-Name</span></span>
<span data-ttu-id="a8ae6-119">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="a8ae6-119">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ae6-120">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="a8ae6-120">-Overwrite</span></span>
<span data-ttu-id="a8ae6-121">Alternativet överskrivning</span><span class="sxs-lookup"><span data-stu-id="a8ae6-121">Overwrite Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ae6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8ae6-122">-ResourceGroupName</span></span>
<span data-ttu-id="a8ae6-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a8ae6-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ae6-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="a8ae6-124">-Slot</span></span>
<span data-ttu-id="a8ae6-125">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="a8ae6-125">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ae6-126">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="a8ae6-126">-StorageAccountUrl</span></span>
<span data-ttu-id="a8ae6-127">URL för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="a8ae6-127">Storage Account Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ae6-128">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a8ae6-128">-WebApp</span></span>
<span data-ttu-id="a8ae6-129">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="a8ae6-129">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ae6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ae6-130">-DefaultProfile</span></span>
<span data-ttu-id="a8ae6-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ae6-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8ae6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ae6-132">CommonParameters</span></span>
<span data-ttu-id="a8ae6-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8ae6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ae6-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8ae6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ae6-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8ae6-135">INPUTS</span></span>

### <span data-ttu-id="a8ae6-136">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="a8ae6-136">Site</span></span>
<span data-ttu-id="a8ae6-137">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a8ae6-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a8ae6-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8ae6-138">OUTPUTS</span></span>

## <span data-ttu-id="a8ae6-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8ae6-139">NOTES</span></span>

## <span data-ttu-id="a8ae6-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8ae6-140">RELATED LINKS</span></span>

