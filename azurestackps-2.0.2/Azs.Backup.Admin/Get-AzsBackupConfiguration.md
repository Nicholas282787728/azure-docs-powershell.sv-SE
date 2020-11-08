---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 3a9fedc637f8400b952d823a98dfe0abaa1d40d3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100271"
---
# <span data-ttu-id="76db8-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="76db8-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="76db8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76db8-102">SYNOPSIS</span></span>
<span data-ttu-id="76db8-103">Returnerar en specifik plats för säkerhets kopior baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="76db8-103">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="76db8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76db8-104">SYNTAX</span></span>

### <span data-ttu-id="76db8-105">Skaffa (standard)</span><span class="sxs-lookup"><span data-stu-id="76db8-105">Get (Default)</span></span>
```
Get-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="76db8-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="76db8-106">GetViaIdentity</span></span>
```
Get-AzsBackupConfiguration -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="76db8-107">Förteckning</span><span class="sxs-lookup"><span data-stu-id="76db8-107">List</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="76db8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76db8-108">DESCRIPTION</span></span>
<span data-ttu-id="76db8-109">Returnerar en specifik plats för säkerhets kopior baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="76db8-109">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="76db8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76db8-110">EXAMPLES</span></span>

### <span data-ttu-id="76db8-111">Exempel 1: Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="76db8-111">Example 1: Get-AzsBackupConfiguration</span></span>
```powershell
PS C:\> Get-AzsBackupConfiguration

```

<span data-ttu-id="76db8-112">Skaffa Azure Stack backup-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="76db8-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="76db8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76db8-113">PARAMETERS</span></span>

### <span data-ttu-id="76db8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76db8-114">-DefaultProfile</span></span>
<span data-ttu-id="76db8-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="76db8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="76db8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76db8-116">-InputObject</span></span>
<span data-ttu-id="76db8-117">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="76db8-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="76db8-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="76db8-118">-Location</span></span>
<span data-ttu-id="76db8-119">Namn på platsen för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="76db8-119">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="76db8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76db8-120">-ResourceGroupName</span></span>
<span data-ttu-id="76db8-121">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="76db8-121">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="76db8-122">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="76db8-122">-Skip</span></span>
<span data-ttu-id="76db8-123">OData Skip-parameter.</span><span class="sxs-lookup"><span data-stu-id="76db8-123">OData skip parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="76db8-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76db8-124">-SubscriptionId</span></span>
<span data-ttu-id="76db8-125">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="76db8-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="76db8-126">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="76db8-126">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="76db8-127">-Överst</span><span class="sxs-lookup"><span data-stu-id="76db8-127">-Top</span></span>
<span data-ttu-id="76db8-128">OData Top-parameter.</span><span class="sxs-lookup"><span data-stu-id="76db8-128">OData top parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="76db8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76db8-129">CommonParameters</span></span>
<span data-ttu-id="76db8-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76db8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76db8-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76db8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76db8-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76db8-132">INPUTS</span></span>

### <span data-ttu-id="76db8-133">Microsoft. Azure. PowerShell. cmdletar. BackupAdmin. Models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="76db8-133">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="76db8-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76db8-134">OUTPUTS</span></span>

### <span data-ttu-id="76db8-135">Microsoft. Azure. PowerShell. cmdletar. BackupAdmin. Models. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="76db8-135">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="76db8-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76db8-136">NOTES</span></span>

<span data-ttu-id="76db8-137">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="76db8-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="76db8-138">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="76db8-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="76db8-139">INPUTOBJECT <IBackupAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="76db8-139">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="76db8-140">`[Backup <String>]`: Namnet på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="76db8-140">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="76db8-141">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="76db8-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="76db8-142">`[Location <String>]`: Namnet på platsen för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="76db8-142">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="76db8-143">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="76db8-143">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="76db8-144">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="76db8-144">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="76db8-145">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="76db8-145">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="76db8-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76db8-146">RELATED LINKS</span></span>

