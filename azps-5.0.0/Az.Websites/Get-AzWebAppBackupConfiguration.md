---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 8ef8639c2ff79a326a8d0ffcdf1f1dca24dbccf9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322560"
---
# <span data-ttu-id="d9ca9-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9ca9-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="d9ca9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9ca9-102">SYNOPSIS</span></span>

## <span data-ttu-id="d9ca9-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9ca9-103">SYNTAX</span></span>

### <span data-ttu-id="d9ca9-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="d9ca9-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9ca9-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="d9ca9-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9ca9-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9ca9-106">DESCRIPTION</span></span>
<span data-ttu-id="d9ca9-107">Cmdleten **Get-AzWebAppBackupConfiguration** hämtar säkerhets kopierings konfigurationen för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d9ca9-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="d9ca9-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9ca9-108">EXAMPLES</span></span>

### <span data-ttu-id="d9ca9-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d9ca9-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="d9ca9-110">Med det här kommandot får du säkerhets kopian från webb programmet som heter WebAppStandard som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="d9ca9-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d9ca9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9ca9-111">PARAMETERS</span></span>

### <span data-ttu-id="d9ca9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ca9-112">-DefaultProfile</span></span>
<span data-ttu-id="d9ca9-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d9ca9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9ca9-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="d9ca9-114">-Name</span></span>
<span data-ttu-id="d9ca9-115">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="d9ca9-115">WebApp Name</span></span>

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

### <span data-ttu-id="d9ca9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9ca9-116">-ResourceGroupName</span></span>
<span data-ttu-id="d9ca9-117">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d9ca9-117">Resource Group Name</span></span>

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

### <span data-ttu-id="d9ca9-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="d9ca9-118">-Slot</span></span>
<span data-ttu-id="d9ca9-119">Plats namn</span><span class="sxs-lookup"><span data-stu-id="d9ca9-119">Slot Name</span></span>

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

### <span data-ttu-id="d9ca9-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d9ca9-120">-WebApp</span></span>
<span data-ttu-id="d9ca9-121">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="d9ca9-121">WebApp Name</span></span>

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

### <span data-ttu-id="d9ca9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ca9-122">CommonParameters</span></span>
<span data-ttu-id="d9ca9-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9ca9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ca9-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9ca9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ca9-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9ca9-125">INPUTS</span></span>

### <span data-ttu-id="d9ca9-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d9ca9-126">System.String</span></span>

### <span data-ttu-id="d9ca9-127">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="d9ca9-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d9ca9-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9ca9-128">OUTPUTS</span></span>

### <span data-ttu-id="d9ca9-129">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9ca9-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="d9ca9-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9ca9-130">NOTES</span></span>

## <span data-ttu-id="d9ca9-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9ca9-131">RELATED LINKS</span></span>
