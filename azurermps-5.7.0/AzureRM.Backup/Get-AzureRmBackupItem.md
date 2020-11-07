---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 8A638FB1-F530-4E28-BAAE-5382671092C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
ms.openlocfilehash: 892e9385a34f9c02ddcf41d57578bb320d645e0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586131"
---
# <span data-ttu-id="b7f14-101">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="b7f14-101">Get-AzureRmBackupItem</span></span>

## <span data-ttu-id="b7f14-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7f14-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f14-103">Hämtar objekten under en behållare i säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="b7f14-103">Gets the items under a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7f14-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7f14-104">SYNTAX</span></span>

```
Get-AzureRmBackupItem [-ProtectionStatus <String>] [-Status <String>] [-Type <String>]
 [-Container] <AzureRMBackupContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7f14-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7f14-105">DESCRIPTION</span></span>
<span data-ttu-id="b7f14-106">Cmdleten **Get-AzureRmBackupItem** hämtar objekten i en behållare i Azure Backup och objektets skydds status.</span><span class="sxs-lookup"><span data-stu-id="b7f14-106">The **Get-AzureRmBackupItem** cmdlet gets the items in a container in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="b7f14-107">Aktivera objekt för skydd med hjälp av Enable-AzureRmBackupProtection cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7f14-107">Enable items for protection by using the Enable-AzureRmBackupProtection cmdlet.</span></span>

<span data-ttu-id="b7f14-108">En behållare som är registrerad för ett säkerhets kopierings valv kan innehålla ett eller flera objekt som kan skyddas.</span><span class="sxs-lookup"><span data-stu-id="b7f14-108">A container that is registered to a Backup vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="b7f14-109">För virtuella Azure-datorer kan det bara finnas ett objekt i behållaren virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b7f14-109">For Azure virtual machines, there can be only one item in the virtual machine container.</span></span>

## <span data-ttu-id="b7f14-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7f14-110">EXAMPLES</span></span>

### <span data-ttu-id="b7f14-111">Exempel 1: Hämta objekten i en behållare</span><span class="sxs-lookup"><span data-stu-id="b7f14-111">Example 1: Get the items in a container</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container
Name                    ProtectionStatus       DataSourceStatus       RecoveryPointsCount    ProtectionPolicyName
----                    ----------------       ----------------       -------------------    --------------------
co03-vm                 NotProtected                                  0
```

<span data-ttu-id="b7f14-112">Det första kommandot får valvet med namnet Vault03 med hjälp av Get-AzureRmBackupVault cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7f14-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="b7f14-113">Kommandot lagrar objektet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="b7f14-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="b7f14-114">Det andra kommandot får en behållare som har det angivna namnet i valvet i $Vault genom att använda cmdleten **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="b7f14-114">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="b7f14-115">Kommandot lagrar objektet i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="b7f14-115">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="b7f14-116">Det slutliga kommandot hämtar säkerhets kopian i behållaren i $Container.</span><span class="sxs-lookup"><span data-stu-id="b7f14-116">The final command gets the backup item in the container in $Container.</span></span>

### <span data-ttu-id="b7f14-117">Exempel 2: Visa alla egenskaper för ett objekt</span><span class="sxs-lookup"><span data-stu-id="b7f14-117">Example 2: View all properties for an item</span></span>
```
PS C:\>Get-AzureRmBackupItem -Container $Container | Select-Object -Property *
Name                 : co03-vm
DataSourceStatus     : 
ProtectionStatus     : NotProtected
Type                 : AzureVM
ProtectionPolicyName : 
ProtectionPolicyId   : 
RecoveryPointsCount  : 0
ItemName             : iaasvmcontainer;co03-vm;co03-vm
ContainerType        : AzureVM
ContainerUniqueName  : iaasvmcontainer;co03-vm;co03-vm
ResourceGroupName    : resourcegroup02
ResourceName         : vault03
Location             : southeastasia
```

<span data-ttu-id="b7f14-118">Det här kommandot får säkerhets kopian i behållaren i $Container och skickar den sedan till Select-Object cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7f14-118">This command gets the backup item in the container in $Container, and then passes it to the Select-Object cmdlet.</span></span>
<span data-ttu-id="b7f14-119">Denna cmdlet returnerar alla egenskaper för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="b7f14-119">That cmdlet returns all properties of the backup item.</span></span>
<span data-ttu-id="b7f14-120">Om du vill ha mer information skriver du `Get-Help Select-Object` .</span><span class="sxs-lookup"><span data-stu-id="b7f14-120">For more information, type `Get-Help Select-Object`.</span></span>

## <span data-ttu-id="b7f14-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7f14-121">PARAMETERS</span></span>

### <span data-ttu-id="b7f14-122">-Container</span><span class="sxs-lookup"><span data-stu-id="b7f14-122">-Container</span></span>
<span data-ttu-id="b7f14-123">Anger ett Container-objekt som denna cmdlet ska säkerhetskopiera objekt för.</span><span class="sxs-lookup"><span data-stu-id="b7f14-123">Specifies a container object for which this cmdlet gets backup items.</span></span>
<span data-ttu-id="b7f14-124">För att få en **AzureRmBackupContainer** , Använd cmdleten Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="b7f14-124">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f14-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f14-125">-DefaultProfile</span></span>
<span data-ttu-id="b7f14-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b7f14-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7f14-127">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="b7f14-127">-ProtectionStatus</span></span>
<span data-ttu-id="b7f14-128">Anger det allmänna skydds statusvärdet för ett objekt i behållaren.</span><span class="sxs-lookup"><span data-stu-id="b7f14-128">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="b7f14-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b7f14-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b7f14-130">Upphovsrättsskydd</span><span class="sxs-lookup"><span data-stu-id="b7f14-130">Protected</span></span> 
- <span data-ttu-id="b7f14-131">Lösenordsskydd</span><span class="sxs-lookup"><span data-stu-id="b7f14-131">Protecting</span></span>  
- <span data-ttu-id="b7f14-132">NotProtected</span><span class="sxs-lookup"><span data-stu-id="b7f14-132">NotProtected</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Protected, Protecting, NotProtected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7f14-133">-Status</span><span class="sxs-lookup"><span data-stu-id="b7f14-133">-Status</span></span>
<span data-ttu-id="b7f14-134">Anger säkerhets kopians status för ett objekt.</span><span class="sxs-lookup"><span data-stu-id="b7f14-134">Specifies the backup status for an item.</span></span>
<span data-ttu-id="b7f14-135">De acceptabla värdena för den här parametern är: IRPending, protected, ProtectionError och ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="b7f14-135">The acceptable values for this parameter are: IRPending, Protected, ProtectionError, and ProtectionStopped.</span></span>
<span data-ttu-id="b7f14-136">Om parametern *ProtectionStatus* har värdet skyddat kan du använda värdet för kommandot *status* för att filtrera objekt.</span><span class="sxs-lookup"><span data-stu-id="b7f14-136">If the *ProtectionStatus* parameter has the value Protected, you can use the *Status* parameter value to filter items.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionStopped, ProtectionError, Protected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7f14-137">– Skriv</span><span class="sxs-lookup"><span data-stu-id="b7f14-137">-Type</span></span>
<span data-ttu-id="b7f14-138">Anger den typ av objekt som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="b7f14-138">Specifies the type of item that this cmdlet gets.</span></span>
<span data-ttu-id="b7f14-139">För närvarande är det enda värdet som stöds AzureVM.</span><span class="sxs-lookup"><span data-stu-id="b7f14-139">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7f14-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f14-140">CommonParameters</span></span>
<span data-ttu-id="b7f14-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7f14-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f14-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7f14-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f14-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7f14-143">INPUTS</span></span>

### <span data-ttu-id="b7f14-144">AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b7f14-144">AzureRmBackupContainer</span></span>

## <span data-ttu-id="b7f14-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7f14-145">OUTPUTS</span></span>

### <span data-ttu-id="b7f14-146">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="b7f14-146">AzureRmBackupItem</span></span>

## <span data-ttu-id="b7f14-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7f14-147">NOTES</span></span>

## <span data-ttu-id="b7f14-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7f14-148">RELATED LINKS</span></span>

[<span data-ttu-id="b7f14-149">Säkerhets kopiering-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="b7f14-149">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="b7f14-150">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="b7f14-150">Disable-AzureRmBackupProtection</span></span>](./Disable-AzureRmBackupProtection.md)

[<span data-ttu-id="b7f14-151">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="b7f14-151">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="b7f14-152">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b7f14-152">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="b7f14-153">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b7f14-153">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="b7f14-154">Återställ-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="b7f14-154">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)

