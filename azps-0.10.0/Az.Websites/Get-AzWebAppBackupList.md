---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: 057bebde5eada143c9ee00260a1406fdceae9436
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923370"
---
# <span data-ttu-id="de0bf-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="de0bf-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="de0bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de0bf-102">SYNOPSIS</span></span>

## <span data-ttu-id="de0bf-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de0bf-103">SYNTAX</span></span>

### <span data-ttu-id="de0bf-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="de0bf-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de0bf-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="de0bf-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de0bf-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de0bf-106">DESCRIPTION</span></span>
<span data-ttu-id="de0bf-107">Cmdleten **Get-AzWebAppBackupList** hämtar en lista över säkerhets kopior för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="de0bf-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="de0bf-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de0bf-108">EXAMPLES</span></span>

### <span data-ttu-id="de0bf-109">9.1</span><span class="sxs-lookup"><span data-stu-id="de0bf-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="de0bf-110">Det här kommandot returnerar en säkerhets kopierings lista som hör till WebApp-WebAppStandard som är kopplad till resurs grupps ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="de0bf-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="de0bf-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de0bf-111">PARAMETERS</span></span>

### <span data-ttu-id="de0bf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de0bf-112">-DefaultProfile</span></span>
<span data-ttu-id="de0bf-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="de0bf-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de0bf-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="de0bf-114">-Name</span></span>
<span data-ttu-id="de0bf-115">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="de0bf-115">WebApp Name</span></span>

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

### <span data-ttu-id="de0bf-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de0bf-116">-ResourceGroupName</span></span>
<span data-ttu-id="de0bf-117">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="de0bf-117">Resource Group Name</span></span>

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

### <span data-ttu-id="de0bf-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="de0bf-118">-Slot</span></span>
<span data-ttu-id="de0bf-119">Plats namn</span><span class="sxs-lookup"><span data-stu-id="de0bf-119">Slot name</span></span>

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

### <span data-ttu-id="de0bf-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="de0bf-120">-WebApp</span></span>
<span data-ttu-id="de0bf-121">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="de0bf-121">Piped WebApp</span></span>

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

### <span data-ttu-id="de0bf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de0bf-122">CommonParameters</span></span>
<span data-ttu-id="de0bf-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de0bf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de0bf-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de0bf-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de0bf-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de0bf-125">INPUTS</span></span>

### <span data-ttu-id="de0bf-126">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="de0bf-126">Site</span></span>
<span data-ttu-id="de0bf-127">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="de0bf-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="de0bf-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de0bf-128">OUTPUTS</span></span>

### <span data-ttu-id="de0bf-129">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="de0bf-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="de0bf-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de0bf-130">NOTES</span></span>

## <span data-ttu-id="de0bf-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de0bf-131">RELATED LINKS</span></span>
