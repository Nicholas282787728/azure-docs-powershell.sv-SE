---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: f4ed396f1abbd8a123bb0e765e288c1ae55d25fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921060"
---
# <span data-ttu-id="c02d6-101">New-AzWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="c02d6-101">New-AzWebAppAzureStoragePath</span></span>

## <span data-ttu-id="c02d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c02d6-102">SYNOPSIS</span></span>
<span data-ttu-id="c02d6-103">Skapar ett objekt som representerar en Azure Storage-sökväg som ska monteras i ett webb program.</span><span class="sxs-lookup"><span data-stu-id="c02d6-103">Creates an object that represents an Azure Storage path to be mounted in a Web App.</span></span> <span data-ttu-id="c02d6-104">Det är avsett att användas som en parameter (-AzureStoragePath) för att Set-AzWebApp och Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c02d6-104">It is meant to be used as a parameter (-AzureStoragePath) to Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <span data-ttu-id="c02d6-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c02d6-105">SYNTAX</span></span>

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c02d6-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c02d6-106">DESCRIPTION</span></span>
<span data-ttu-id="c02d6-107">Skapar ett objekt som representerar en Azure-lagringsenhet som ska monteras i ett webb program.</span><span class="sxs-lookup"><span data-stu-id="c02d6-107">Creates an object that represent an Azure Storage path to be mounted inside a Web App.</span></span>

## <span data-ttu-id="c02d6-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c02d6-108">EXAMPLES</span></span>

### <span data-ttu-id="c02d6-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c02d6-109">Example 1</span></span>
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## <span data-ttu-id="c02d6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c02d6-110">PARAMETERS</span></span>

### <span data-ttu-id="c02d6-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="c02d6-111">-AccessKey</span></span>
<span data-ttu-id="c02d6-112">Åtkomst till Azure Storage-kontot</span><span class="sxs-lookup"><span data-stu-id="c02d6-112">Access key to the Azure Storage account</span></span>

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

### <span data-ttu-id="c02d6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c02d6-113">-AccountName</span></span>
<span data-ttu-id="c02d6-114">Namn på Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="c02d6-114">Azure Storage account name.</span></span>
<span data-ttu-id="c02d6-115">T. ex.: myfilestorageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="c02d6-115">E.g.: myfilestorageaccount.file.core.windows.net</span></span>

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

### <span data-ttu-id="c02d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c02d6-116">-DefaultProfile</span></span>
<span data-ttu-id="c02d6-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c02d6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c02d6-118">-MountPath</span><span class="sxs-lookup"><span data-stu-id="c02d6-118">-MountPath</span></span>
<span data-ttu-id="c02d6-119">Sökvägen i behållaren där resursen som anges av resurs namn ska visas</span><span class="sxs-lookup"><span data-stu-id="c02d6-119">Path in the container where the share specified by ShareName will be exposed</span></span>

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

### <span data-ttu-id="c02d6-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="c02d6-120">-Name</span></span>
<span data-ttu-id="c02d6-121">ID för Azure Storage-egenskapen.</span><span class="sxs-lookup"><span data-stu-id="c02d6-121">The identifier of the Azure Storage property.</span></span>
<span data-ttu-id="c02d6-122">Måste vara unikt inom webb programmet eller plats</span><span class="sxs-lookup"><span data-stu-id="c02d6-122">Must be unique within the Web App or Slot</span></span>

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

### <span data-ttu-id="c02d6-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c02d6-123">-ShareName</span></span>
<span data-ttu-id="c02d6-124">Namn på resursen som ska monteras i behållaren</span><span class="sxs-lookup"><span data-stu-id="c02d6-124">Name of the share to mount to the container</span></span>

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

### <span data-ttu-id="c02d6-125">– Skriv</span><span class="sxs-lookup"><span data-stu-id="c02d6-125">-Type</span></span>
<span data-ttu-id="c02d6-126">Typ av Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="c02d6-126">Type of Azure Storage account.</span></span>
<span data-ttu-id="c02d6-127">Windows-behållare stöder bara Azure-filer</span><span class="sxs-lookup"><span data-stu-id="c02d6-127">Windows Containers only supports Azure Files</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.AzureStorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureFiles, AzureBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c02d6-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c02d6-128">-Confirm</span></span>
<span data-ttu-id="c02d6-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c02d6-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c02d6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c02d6-130">-WhatIf</span></span>
<span data-ttu-id="c02d6-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c02d6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c02d6-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c02d6-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c02d6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c02d6-133">CommonParameters</span></span>
<span data-ttu-id="c02d6-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c02d6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c02d6-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c02d6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c02d6-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c02d6-136">INPUTS</span></span>

### <span data-ttu-id="c02d6-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="c02d6-137">None</span></span>

## <span data-ttu-id="c02d6-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c02d6-138">OUTPUTS</span></span>

### <span data-ttu-id="c02d6-139">Microsoft. Azure. commands. webapps. Models. WebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="c02d6-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span></span>

## <span data-ttu-id="c02d6-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c02d6-140">NOTES</span></span>

## <span data-ttu-id="c02d6-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c02d6-141">RELATED LINKS</span></span>
