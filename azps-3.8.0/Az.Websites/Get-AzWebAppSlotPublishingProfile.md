---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 249ecef690fa4eaf59e6a7de97a75d55a285b377
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089572"
---
# <span data-ttu-id="e17cc-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="e17cc-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="e17cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e17cc-102">SYNOPSIS</span></span>
<span data-ttu-id="e17cc-103">Hämtar en Azure Web App slot-publicerings profil.</span><span class="sxs-lookup"><span data-stu-id="e17cc-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="e17cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e17cc-104">SYNTAX</span></span>

### <span data-ttu-id="e17cc-105">S</span><span class="sxs-lookup"><span data-stu-id="e17cc-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e17cc-106">S2</span><span class="sxs-lookup"><span data-stu-id="e17cc-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e17cc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e17cc-107">DESCRIPTION</span></span>
<span data-ttu-id="e17cc-108">Cmdleten **Get-AzWebAppSlotPublishingProfile** hämtar webb program publicerings profilen för den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="e17cc-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="e17cc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e17cc-109">EXAMPLES</span></span>

### <span data-ttu-id="e17cc-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e17cc-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="e17cc-111">Det här kommandot får publicerings profilen i FTP-format för fack Slot001 som hör till Web App-ContosoWebApp som är kopplat till resurs gruppens standard-väst och lagrar den i den angivna utdatafilen.</span><span class="sxs-lookup"><span data-stu-id="e17cc-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="e17cc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e17cc-112">PARAMETERS</span></span>

### <span data-ttu-id="e17cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e17cc-113">-DefaultProfile</span></span>
<span data-ttu-id="e17cc-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e17cc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e17cc-115">-Format</span><span class="sxs-lookup"><span data-stu-id="e17cc-115">-Format</span></span>
<span data-ttu-id="e17cc-116">Format</span><span class="sxs-lookup"><span data-stu-id="e17cc-116">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e17cc-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="e17cc-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="e17cc-118">Inkludera slut punkter för återställning av katastrof om sant</span><span class="sxs-lookup"><span data-stu-id="e17cc-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="e17cc-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="e17cc-119">-Name</span></span>
<span data-ttu-id="e17cc-120">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="e17cc-120">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17cc-121">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="e17cc-121">-OutputFile</span></span>
<span data-ttu-id="e17cc-122">Utdatafil</span><span class="sxs-lookup"><span data-stu-id="e17cc-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e17cc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e17cc-123">-ResourceGroupName</span></span>
<span data-ttu-id="e17cc-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="e17cc-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e17cc-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="e17cc-125">-Slot</span></span>
<span data-ttu-id="e17cc-126">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="e17cc-126">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e17cc-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e17cc-127">-WebApp</span></span>
<span data-ttu-id="e17cc-128">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="e17cc-128">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e17cc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e17cc-129">CommonParameters</span></span>
<span data-ttu-id="e17cc-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e17cc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e17cc-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e17cc-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e17cc-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e17cc-132">INPUTS</span></span>

### <span data-ttu-id="e17cc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e17cc-133">System.String</span></span>

### <span data-ttu-id="e17cc-134">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="e17cc-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e17cc-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e17cc-135">OUTPUTS</span></span>

### <span data-ttu-id="e17cc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e17cc-136">System.String</span></span>

## <span data-ttu-id="e17cc-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e17cc-137">NOTES</span></span>

## <span data-ttu-id="e17cc-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e17cc-138">RELATED LINKS</span></span>

[<span data-ttu-id="e17cc-139">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="e17cc-139">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="e17cc-140">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e17cc-140">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="e17cc-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e17cc-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)