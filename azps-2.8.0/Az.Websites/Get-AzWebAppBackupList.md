---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: fab8973c63e419cdef45fb79a0ad5182c46f2de5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921139"
---
# <span data-ttu-id="fbf02-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="fbf02-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="fbf02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fbf02-102">SYNOPSIS</span></span>

## <span data-ttu-id="fbf02-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fbf02-103">SYNTAX</span></span>

### <span data-ttu-id="fbf02-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="fbf02-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbf02-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="fbf02-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbf02-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fbf02-106">DESCRIPTION</span></span>
<span data-ttu-id="fbf02-107">Cmdleten **Get-AzWebAppBackupList** hämtar en lista över säkerhets kopior för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="fbf02-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="fbf02-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fbf02-108">EXAMPLES</span></span>

### <span data-ttu-id="fbf02-109">9.1</span><span class="sxs-lookup"><span data-stu-id="fbf02-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="fbf02-110">Det här kommandot returnerar en säkerhets kopierings lista som hör till WebApp-WebAppStandard som är kopplad till resurs grupps ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fbf02-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="fbf02-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fbf02-111">PARAMETERS</span></span>

### <span data-ttu-id="fbf02-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbf02-112">-DefaultProfile</span></span>
<span data-ttu-id="fbf02-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fbf02-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbf02-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="fbf02-114">-Name</span></span>
<span data-ttu-id="fbf02-115">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="fbf02-115">WebApp Name</span></span>

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

### <span data-ttu-id="fbf02-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbf02-116">-ResourceGroupName</span></span>
<span data-ttu-id="fbf02-117">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="fbf02-117">Resource Group Name</span></span>

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

### <span data-ttu-id="fbf02-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="fbf02-118">-Slot</span></span>
<span data-ttu-id="fbf02-119">Plats namn</span><span class="sxs-lookup"><span data-stu-id="fbf02-119">Slot name</span></span>

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

### <span data-ttu-id="fbf02-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fbf02-120">-WebApp</span></span>
<span data-ttu-id="fbf02-121">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="fbf02-121">Piped WebApp</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbf02-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbf02-122">CommonParameters</span></span>
<span data-ttu-id="fbf02-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbf02-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbf02-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbf02-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbf02-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fbf02-125">INPUTS</span></span>

### <span data-ttu-id="fbf02-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fbf02-126">System.String</span></span>

### <span data-ttu-id="fbf02-127">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="fbf02-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="fbf02-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fbf02-128">OUTPUTS</span></span>

### <span data-ttu-id="fbf02-129">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="fbf02-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="fbf02-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fbf02-130">NOTES</span></span>

## <span data-ttu-id="fbf02-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fbf02-131">RELATED LINKS</span></span>
