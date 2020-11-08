---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackup
schema: 2.0.0
ms.openlocfilehash: 2c2d517da3be62ff407ca17577edefcf7322ad55
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94093081"
---
# <span data-ttu-id="35c0a-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="35c0a-101">Get-AzsBackup</span></span>

## <span data-ttu-id="35c0a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="35c0a-103">Returnerar en säkerhets kopia från en plats baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="35c0a-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="35c0a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35c0a-104">SYNTAX</span></span>

### <span data-ttu-id="35c0a-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="35c0a-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="35c0a-106">Lära</span><span class="sxs-lookup"><span data-stu-id="35c0a-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="35c0a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="35c0a-107">GetViaIdentity</span></span>
```
Get-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="35c0a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35c0a-108">DESCRIPTION</span></span>
<span data-ttu-id="35c0a-109">Returnerar en säkerhets kopia från en plats baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="35c0a-109">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="35c0a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35c0a-110">EXAMPLES</span></span>

### <span data-ttu-id="35c0a-111">Exempel 1: lista säkerhets kopior</span><span class="sxs-lookup"><span data-stu-id="35c0a-111">Example 1: List Backups</span></span>
```powershell
PS C:\> Get-AzsBackup

```

<span data-ttu-id="35c0a-112">Få information sbout alla säkerhets kopior av Azure-stacken.</span><span class="sxs-lookup"><span data-stu-id="35c0a-112">Get information sbout all Azure Stack backups.</span></span>

### <span data-ttu-id="35c0a-113">Exempel 2: Hämta specifik säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="35c0a-113">Example 2: Get specific backup</span></span>
```powershell
PS C:\> Get-AzsBackup -Name 'backupName'

```

<span data-ttu-id="35c0a-114">Få information för den angivna Azure-stacken.</span><span class="sxs-lookup"><span data-stu-id="35c0a-114">Get information for the the specified Azure Stack backup.</span></span>

## <span data-ttu-id="35c0a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35c0a-115">PARAMETERS</span></span>

### <span data-ttu-id="35c0a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35c0a-116">-DefaultProfile</span></span>
<span data-ttu-id="35c0a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="35c0a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35c0a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35c0a-118">-InputObject</span></span>
<span data-ttu-id="35c0a-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="35c0a-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="35c0a-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="35c0a-120">-Location</span></span>
<span data-ttu-id="35c0a-121">Namn på platsen för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="35c0a-121">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="35c0a-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="35c0a-122">-Name</span></span>
<span data-ttu-id="35c0a-123">Namn på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="35c0a-123">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="35c0a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35c0a-124">-ResourceGroupName</span></span>
<span data-ttu-id="35c0a-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="35c0a-125">Name of the resource group.</span></span>

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

### <span data-ttu-id="35c0a-126">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="35c0a-126">-Skip</span></span>
<span data-ttu-id="35c0a-127">OData Skip-parameter.</span><span class="sxs-lookup"><span data-stu-id="35c0a-127">OData skip parameter.</span></span>

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

### <span data-ttu-id="35c0a-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35c0a-128">-SubscriptionId</span></span>
<span data-ttu-id="35c0a-129">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="35c0a-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="35c0a-130">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="35c0a-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="35c0a-131">-Överst</span><span class="sxs-lookup"><span data-stu-id="35c0a-131">-Top</span></span>
<span data-ttu-id="35c0a-132">OData Top-parameter.</span><span class="sxs-lookup"><span data-stu-id="35c0a-132">OData top parameter.</span></span>

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

### <span data-ttu-id="35c0a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35c0a-133">CommonParameters</span></span>
<span data-ttu-id="35c0a-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35c0a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35c0a-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35c0a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35c0a-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35c0a-136">INPUTS</span></span>

### <span data-ttu-id="35c0a-137">Microsoft. Azure. PowerShell. cmdletar. BackupAdmin. Models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="35c0a-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="35c0a-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35c0a-138">OUTPUTS</span></span>

### <span data-ttu-id="35c0a-139">Microsoft. Azure. PowerShell. cmdletar. BackupAdmin. Models. Api20180901. IBackup</span><span class="sxs-lookup"><span data-stu-id="35c0a-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="35c0a-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35c0a-140">NOTES</span></span>

<span data-ttu-id="35c0a-141">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="35c0a-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35c0a-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="35c0a-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="35c0a-143">INPUTOBJECT <IBackupAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="35c0a-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="35c0a-144">`[Backup <String>]`: Namnet på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="35c0a-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="35c0a-145">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="35c0a-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="35c0a-146">`[Location <String>]`: Namnet på platsen för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="35c0a-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="35c0a-147">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="35c0a-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="35c0a-148">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="35c0a-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="35c0a-149">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="35c0a-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="35c0a-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35c0a-150">RELATED LINKS</span></span>

