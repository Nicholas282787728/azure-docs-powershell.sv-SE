---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
ms.openlocfilehash: 51fc1b96734d269fda3e09d3a22122b18fe3943a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581331"
---
# <span data-ttu-id="80daf-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="80daf-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="80daf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80daf-102">SYNOPSIS</span></span>
<span data-ttu-id="80daf-103">Får ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="80daf-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80daf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80daf-104">SYNTAX</span></span>

### <span data-ttu-id="80daf-105">Ett lås i resurs gruppens omfattning.</span><span class="sxs-lookup"><span data-stu-id="80daf-105">A lock at the resource group scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="80daf-106">Ett lås i resurs gruppens resurs omfång.</span><span class="sxs-lookup"><span data-stu-id="80daf-106">A lock at the resource group resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="80daf-107">Ett lås vid det angivna omfånget.</span><span class="sxs-lookup"><span data-stu-id="80daf-107">A lock at the specified scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="80daf-108">Ett lås i prenumerations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="80daf-108">A lock at the subscription scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="80daf-109">Ett lås i resurs omfattningen för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="80daf-109">A lock at the subscription resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="80daf-110">Ett lås hos klient organisationens omfattning.</span><span class="sxs-lookup"><span data-stu-id="80daf-110">A lock at the tenant resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="80daf-111">Ett lås, efter ID.</span><span class="sxs-lookup"><span data-stu-id="80daf-111">A lock, by Id.</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="80daf-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80daf-112">DESCRIPTION</span></span>
<span data-ttu-id="80daf-113">Cmdleten **Get-AzureRmResourceLock** får Azure Resource lock.</span><span class="sxs-lookup"><span data-stu-id="80daf-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="80daf-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80daf-114">EXAMPLES</span></span>

### <span data-ttu-id="80daf-115">Exempel 1: skaffa ett lås</span><span class="sxs-lookup"><span data-stu-id="80daf-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="80daf-116">Det här kommandot får resurs låset med namnet ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="80daf-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="80daf-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80daf-117">PARAMETERS</span></span>

### <span data-ttu-id="80daf-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="80daf-118">-ApiVersion</span></span>
<span data-ttu-id="80daf-119">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="80daf-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="80daf-120">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="80daf-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80daf-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="80daf-121">-AtScope</span></span>
<span data-ttu-id="80daf-122">Anger att denna cmdlet returnerar alla lås på eller ovanför det angivna omfånget.</span><span class="sxs-lookup"><span data-stu-id="80daf-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="80daf-123">Om du inte anger den här parametern returnerar cmdleten alla lås på, ovanför eller under scopet.</span><span class="sxs-lookup"><span data-stu-id="80daf-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="80daf-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="80daf-124">-InformationAction</span></span>
<span data-ttu-id="80daf-125">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="80daf-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="80daf-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="80daf-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80daf-127">Vidare</span><span class="sxs-lookup"><span data-stu-id="80daf-127">Continue</span></span>
- <span data-ttu-id="80daf-128">Över</span><span class="sxs-lookup"><span data-stu-id="80daf-128">Ignore</span></span>
- <span data-ttu-id="80daf-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="80daf-129">Inquire</span></span>
- <span data-ttu-id="80daf-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="80daf-130">SilentlyContinue</span></span>
- <span data-ttu-id="80daf-131">Stanna</span><span class="sxs-lookup"><span data-stu-id="80daf-131">Stop</span></span>
- <span data-ttu-id="80daf-132">Avbryt</span><span class="sxs-lookup"><span data-stu-id="80daf-132">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80daf-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="80daf-133">-InformationVariable</span></span>
<span data-ttu-id="80daf-134">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="80daf-134">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80daf-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="80daf-135">-LockId</span></span>
<span data-ttu-id="80daf-136">Anger ID för det lås som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="80daf-136">Specifies the ID of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock, by Id.
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80daf-137">-LockName</span><span class="sxs-lookup"><span data-stu-id="80daf-137">-LockName</span></span>
<span data-ttu-id="80daf-138">Anger namnet på det lås som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="80daf-138">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope., A lock at the specified scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80daf-139">-För</span><span class="sxs-lookup"><span data-stu-id="80daf-139">-Pre</span></span>
<span data-ttu-id="80daf-140">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="80daf-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="80daf-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80daf-141">-ResourceGroupName</span></span>
<span data-ttu-id="80daf-142">Anger namnet på den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="80daf-142">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="80daf-143">Denna cmdlet hämtar lås för den här resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="80daf-143">This cmdlet gets locks for this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80daf-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="80daf-144">-ResourceName</span></span>
<span data-ttu-id="80daf-145">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="80daf-145">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="80daf-146">Denna cmdlet hämtar lås för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="80daf-146">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80daf-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="80daf-147">-ResourceType</span></span>
<span data-ttu-id="80daf-148">Anger resurs typen för den resurs som den här låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="80daf-148">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="80daf-149">Denna cmdlet hämtar lås för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="80daf-149">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80daf-150">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="80daf-150">-Scope</span></span>
<span data-ttu-id="80daf-151">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="80daf-151">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="80daf-152">Cmdleten får lås för detta scope.</span><span class="sxs-lookup"><span data-stu-id="80daf-152">The cmdlet gets locks for this scope.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80daf-153">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="80daf-153">-TenantLevel</span></span>
<span data-ttu-id="80daf-154">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="80daf-154">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80daf-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80daf-155">-DefaultProfile</span></span>
<span data-ttu-id="80daf-156">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="80daf-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80daf-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80daf-157">CommonParameters</span></span>
<span data-ttu-id="80daf-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80daf-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80daf-159">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80daf-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80daf-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80daf-160">INPUTS</span></span>

## <span data-ttu-id="80daf-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80daf-161">OUTPUTS</span></span>

### <span data-ttu-id="80daf-162">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="80daf-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="80daf-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80daf-163">NOTES</span></span>

## <span data-ttu-id="80daf-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80daf-164">RELATED LINKS</span></span>

[<span data-ttu-id="80daf-165">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="80daf-165">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="80daf-166">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="80daf-166">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="80daf-167">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="80daf-167">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


