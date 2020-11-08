---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
ms.openlocfilehash: a2c57ebe6f85209596628dffe9de88ca260bbafa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090325"
---
# <span data-ttu-id="08627-101">Set-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="08627-101">Set-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="08627-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08627-102">SYNOPSIS</span></span>
<span data-ttu-id="08627-103">Ange webb program plats konfigurations namn</span><span class="sxs-lookup"><span data-stu-id="08627-103">Set Web App Slot Config names</span></span>

## <span data-ttu-id="08627-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08627-104">SYNTAX</span></span>

### <span data-ttu-id="08627-105">S</span><span class="sxs-lookup"><span data-stu-id="08627-105">S1</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08627-106">S2</span><span class="sxs-lookup"><span data-stu-id="08627-106">S2</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08627-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08627-107">DESCRIPTION</span></span>
<span data-ttu-id="08627-108">Cmdleten **set-AzWebAppSlotConfigName** anger program inställningar och anslutnings strängar som plats inställningar</span><span class="sxs-lookup"><span data-stu-id="08627-108">The **Set-AzWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="08627-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08627-109">EXAMPLES</span></span>

### <span data-ttu-id="08627-110">9.1</span><span class="sxs-lookup"><span data-stu-id="08627-110">1:</span></span>
```
PS C:\> Set-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="08627-111">Det här kommandot tar bort alla program inställningar och anslutnings strängar för webb programmet ContosoWebApp som är kopplade till resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="08627-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="08627-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08627-112">PARAMETERS</span></span>

### <span data-ttu-id="08627-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="08627-113">-AppSettingNames</span></span>
<span data-ttu-id="08627-114">Program inställningar namn sträng mat ris</span><span class="sxs-lookup"><span data-stu-id="08627-114">App Settings Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08627-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="08627-115">-ConnectionStringNames</span></span>
<span data-ttu-id="08627-116">Sträng mat ris namn</span><span class="sxs-lookup"><span data-stu-id="08627-116">Connection String Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08627-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08627-117">-DefaultProfile</span></span>
<span data-ttu-id="08627-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="08627-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08627-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="08627-119">-Name</span></span>
<span data-ttu-id="08627-120">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="08627-120">WebApp Name</span></span>

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

### <span data-ttu-id="08627-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="08627-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="08627-122">Alternativet ta bort alla namn för program inställningar</span><span class="sxs-lookup"><span data-stu-id="08627-122">Remove All App Setting Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08627-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="08627-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="08627-124">Ta bort alla namn alternativ för anslutnings strängar</span><span class="sxs-lookup"><span data-stu-id="08627-124">Remove All Connection String Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08627-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08627-125">-ResourceGroupName</span></span>
<span data-ttu-id="08627-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="08627-126">Resource Group Name</span></span>

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

### <span data-ttu-id="08627-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="08627-127">-WebApp</span></span>
<span data-ttu-id="08627-128">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="08627-128">WebApp Object</span></span>

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

### <span data-ttu-id="08627-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08627-129">CommonParameters</span></span>
<span data-ttu-id="08627-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08627-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08627-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08627-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08627-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08627-132">INPUTS</span></span>

### <span data-ttu-id="08627-133">System. string []</span><span class="sxs-lookup"><span data-stu-id="08627-133">System.String[]</span></span>

### <span data-ttu-id="08627-134">System. String</span><span class="sxs-lookup"><span data-stu-id="08627-134">System.String</span></span>

### <span data-ttu-id="08627-135">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="08627-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="08627-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08627-136">OUTPUTS</span></span>

### <span data-ttu-id="08627-137">Microsoft. Azure. Management. webbplatser. Models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="08627-137">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="08627-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08627-138">NOTES</span></span>

## <span data-ttu-id="08627-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08627-139">RELATED LINKS</span></span>
