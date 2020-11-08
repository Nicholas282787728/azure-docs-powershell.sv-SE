---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: e50c711e730f3af79ce5d8825e6beeee9b663e00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102540"
---
# <span data-ttu-id="1a00d-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="1a00d-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="1a00d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a00d-102">SYNOPSIS</span></span>

## <span data-ttu-id="1a00d-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a00d-103">SYNTAX</span></span>

### <span data-ttu-id="1a00d-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1a00d-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a00d-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1a00d-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a00d-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a00d-106">DESCRIPTION</span></span>
<span data-ttu-id="1a00d-107">Cmdleten **Remove-AzWebAppBackup** tar bort den angivna säkerhets kopian av ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1a00d-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="1a00d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a00d-108">EXAMPLES</span></span>

### <span data-ttu-id="1a00d-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1a00d-109">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="1a00d-110">Med det här kommandot tas säkerhets kopian bort med ID för "12345" från webb programmet med namnet WebAppStandard som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="1a00d-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="1a00d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a00d-111">PARAMETERS</span></span>

### <span data-ttu-id="1a00d-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="1a00d-112">-BackupId</span></span>
<span data-ttu-id="1a00d-113">Säkerhets kopie-ID</span><span class="sxs-lookup"><span data-stu-id="1a00d-113">Backup Id</span></span>

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

### <span data-ttu-id="1a00d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a00d-114">-DefaultProfile</span></span>
<span data-ttu-id="1a00d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1a00d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a00d-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="1a00d-116">-Name</span></span>
<span data-ttu-id="1a00d-117">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="1a00d-117">WebApp Name</span></span>

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

### <span data-ttu-id="1a00d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a00d-118">-ResourceGroupName</span></span>
<span data-ttu-id="1a00d-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="1a00d-119">Resource Group Name</span></span>

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

### <span data-ttu-id="1a00d-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="1a00d-120">-Slot</span></span>
<span data-ttu-id="1a00d-121">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="1a00d-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="1a00d-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1a00d-122">-WebApp</span></span>
<span data-ttu-id="1a00d-123">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="1a00d-123">WebApp Object</span></span>

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

### <span data-ttu-id="1a00d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a00d-124">CommonParameters</span></span>
<span data-ttu-id="1a00d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a00d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a00d-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a00d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a00d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a00d-127">INPUTS</span></span>

### <span data-ttu-id="1a00d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1a00d-128">System.String</span></span>

### <span data-ttu-id="1a00d-129">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="1a00d-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1a00d-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a00d-130">OUTPUTS</span></span>

### <span data-ttu-id="1a00d-131">Microsoft. Azure. Management. webbplatser. Models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="1a00d-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="1a00d-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a00d-132">NOTES</span></span>

## <span data-ttu-id="1a00d-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a00d-133">RELATED LINKS</span></span>
