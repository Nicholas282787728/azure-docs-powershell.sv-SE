---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088953"
---
# <span data-ttu-id="9b2d1-101">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="9b2d1-101">Set-AzDataLakeGen2ItemAclObject</span></span>

## <span data-ttu-id="9b2d1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b2d1-102">SYNOPSIS</span></span>
<span data-ttu-id="9b2d1-103">Skapar/uppdaterar ett DataLake-Gen2 objekt, som kan användas i Update-AzDataLakeGen2Item cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-103">Creates/Updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>

## <span data-ttu-id="9b2d1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b2d1-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## <span data-ttu-id="9b2d1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b2d1-105">DESCRIPTION</span></span>
<span data-ttu-id="9b2d1-106">Cmdleten **set-AzDataLakeGen2ItemAclObject** skapar/uppdaterar ett DataLake-objekt, som kan användas i Update-AzDataLakeGen2Item cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-106">The **Set-AzDataLakeGen2ItemAclObject** cmdlet creates/updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>
<span data-ttu-id="9b2d1-107">Om den nya ACL-posten med samma AccessControlType/EntityId/DefaultScope inte finns i indata-ACL: en skapar en ny ACL-post, annars kan du uppdatera behörigheten för befintlig ACL-post.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-107">If the new ACL entry with same AccessControlType/EntityId/DefaultScope not exist in the input ACL, will create a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="9b2d1-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b2d1-108">EXAMPLES</span></span>

### <span data-ttu-id="9b2d1-109">Exempel 1: skapa ett ACL-objekt med 3 ACL-post och uppdatera ACL för en katalog</span><span class="sxs-lookup"><span data-stu-id="9b2d1-109">Example 1: Create an ACL object with 3 ACL entry, and update ACL on a directory</span></span>
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/dir3" -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

<span data-ttu-id="9b2d1-110">Det här kommandot skapar ett ACL-objekt med 3 ACL-poster (Use-InputObject-parametern för att lägga till ACL-posten i befintligt ACL-objekt) och uppdatera ACL för en katalog.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-110">This command creates an ACL object with 3 ACL entries (use -InputObject parameter to add acl entry to existing acl object), and updates ACL on a directory.</span></span>

### <span data-ttu-id="9b2d1-111">Exempel 2: skapa ett ACL-objekt med 4 ACL-poster och uppdatera behörighet för en befintlig ACL-post</span><span class="sxs-lookup"><span data-stu-id="9b2d1-111">Example 2: Create an ACL object with 4 ACL entries, and update permission of an existing ACL entry</span></span>
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rwx -InputObject $acl 
PS C:\>$acl

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ rwx        

PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl 
PS C:\>$acl  

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ r-x
```

<span data-ttu-id="9b2d1-112">Det här kommandot skapar först ett ACL-objekt med 4 ACL-poster och kör cmdleten igen med olika behörigheter men samma AccessControlType/EntityId/DefaultScope för en befintlig ACL-post.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-112">This command first creates an ACL object with 4 ACL entries, then run the cmdlet again with different permission but same AccessControlType/EntityId/DefaultScope of an existing ACL entry.</span></span>
<span data-ttu-id="9b2d1-113">Behörigheten för ACL-posten uppdateras men ingen ny ACL-post läggs till.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-113">Then the permission of the ACL entry is updated, but no new ACL entry is added.</span></span>

## <span data-ttu-id="9b2d1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b2d1-114">PARAMETERS</span></span>

### <span data-ttu-id="9b2d1-115">-AccessControlType</span><span class="sxs-lookup"><span data-stu-id="9b2d1-115">-AccessControlType</span></span>
<span data-ttu-id="9b2d1-116">Det finns fyra typer: "användare" ger rättigheter till ägaren eller en namngiven användare, "grupp" ger rättigheterna till den ägande gruppen eller en namngiven grupp, "mask" begränsar rättigheterna till namngivna användare och medlemmar i grupper och "Övrigt" ger rättigheter till alla användare som inte finns i någon av de andra posterna.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-116">There are four types: "user" grants rights to the owner or a named user, "group" grants rights to the owning group or a named group, "mask" restricts rights granted to named users and the members of groups, and "other" grants rights to all users not found in any of the other entries.</span></span>

```yaml
Type: Azure.Storage.Files.DataLake.Models.AccessControlType
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b2d1-117">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="9b2d1-117">-DefaultScope</span></span>
<span data-ttu-id="9b2d1-118">Ange den här parametern för att ange ACE tillhör standard åtkomst kontroll för en katalog; i övrigt är omfattningen implicit och ACE: en åtkomst kontrol lista.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-118">Set this parameter to indicate the ACE belongs to the default ACL for a directory; otherwise scope is implicit and the ACE belongs to the access ACL.</span></span>

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

### <span data-ttu-id="9b2d1-119">-EntityId</span><span class="sxs-lookup"><span data-stu-id="9b2d1-119">-EntityId</span></span>
<span data-ttu-id="9b2d1-120">ID för användaren eller gruppen.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-120">The user or group identifier.</span></span>
<span data-ttu-id="9b2d1-121">Den utelämnas för AccessControlType "mask" och "Övrigt".</span><span class="sxs-lookup"><span data-stu-id="9b2d1-121">It is omitted for entries of AccessControlType "mask" and "other".</span></span>
<span data-ttu-id="9b2d1-122">Användarens eller gruppens identifierare utelämnas också för gruppen ägare och ägande.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-122">The user or group identifier is also omitted for the owner and owning group.</span></span>

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

### <span data-ttu-id="9b2d1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b2d1-123">-InputObject</span></span>
<span data-ttu-id="9b2d1-124">Om du anger PSPathAccessControlEntry \[ \] -objektet läggs den nya åtkomst kontrol listan till som ett nytt element i PSPathAccessControlEntry- \[ \] objektet.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-124">If input the PSPathAccessControlEntry\[\] object, will add the new ACL as a new element of the input PSPathAccessControlEntry\[\] object.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b2d1-125">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="9b2d1-125">-Permission</span></span>
<span data-ttu-id="9b2d1-126">Behörighets fältet är en sekvens med 3 tecken där det första tecknet är "r" för att bevilja Läs åtkomst, det andra tecknet är "w" för att ge skriv åtkomst och det tredje tecknet är "x" för att ge behörigheten Kör.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-126">The permission field is a 3-character sequence where the first character is 'r' to grant read access, the second character is 'w' to grant write access, and the third character is 'x' to grant execute permission.</span></span>
<span data-ttu-id="9b2d1-127">Om åtkomst inte beviljas används tecknet "-" för att ange att behörigheten nekas.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-127">If access is not granted, the '-' character is used to denote that the permission is denied.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b2d1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b2d1-128">CommonParameters</span></span>
<span data-ttu-id="9b2d1-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b2d1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b2d1-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b2d1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b2d1-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b2d1-131">INPUTS</span></span>

### <span data-ttu-id="9b2d1-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="9b2d1-132">None</span></span>

## <span data-ttu-id="9b2d1-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b2d1-133">OUTPUTS</span></span>

### <span data-ttu-id="9b2d1-134">Microsoft. WindowsAzure. commands. Storage. Model. ResourceModel. PSPathAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="9b2d1-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span></span>

## <span data-ttu-id="9b2d1-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b2d1-135">NOTES</span></span>

## <span data-ttu-id="9b2d1-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b2d1-136">RELATED LINKS</span></span>
